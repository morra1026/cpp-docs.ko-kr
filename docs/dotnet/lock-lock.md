---
title: lock::lock | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- lock::lock
- lock.lock
- msclr.lock.lock
- msclr::lock::lock
dev_langs:
- C++
helpviewer_keywords:
- lock constructor
ms.assetid: c9ad6c71-36ec-49c5-8ebd-f5c3a0cc94f0
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 128a86b59ebf43ab87b0f4f4bcb7e9c684e4ad07
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46051826"
---
# <a name="locklock"></a>lock::lock
생성을 `lock` 또는 전혀 사용 하지 않을 경우의 지정된 된 시간에 대 한 잠금을 영구적으로 획득 하려고 대기 하는 선택적 개체입니다.  
  
## <a name="syntax"></a>구문  
  
```  
template<class T> lock(  
   T ^ _object  
);  
template<class T> lock(  
   T ^ _object,  
   int _timeout  
);  
template<class T> lock(  
   T ^ _object,  
   System::TimeSpan _timeout  
);  
template<class T> lock(  
   T ^ _object,  
   lock_later  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
*(_o)*<br/>
개체를 잠글 수입니다.  
  
*시간 제한 _t*<br/>
시간 (밀리초) 또는 시간 제한 값을 <xref:System.TimeSpan>입니다.  
  
## <a name="exceptions"></a>예외  
 Throw <xref:System.ApplicationException> 잠금 획득 시간 제한 전에 발생 하지 않습니다.  
  
## <a name="remarks"></a>설명  
 생성자의 처음 세 개의 폼에서 잠금을 획득 하려고 `_object` 지정된 된 제한 시간 내에서 (또는 <xref:System.Threading.Timeout.Infinite> 지정 되지 않은 경우).  
  
 네 번째 형식의 생성자에서 잠금을 획득 하지 `_object`합니다. `lock_later` 구성원임을 확인 합니다 [lock_when 열거형](../dotnet/lock-when-enum.md)합니다. 사용 하 여 [lock::acquire](../dotnet/lock-acquire.md) 하거나 [lock::try_acquire](../dotnet/lock-try-acquire.md) 잠금을 획득 하기 위해이 경우.  
  
 소멸자가 호출 될 때에 자동으로 잠금이 해제 됩니다.  
  
 `_object`가 <xref:System.Threading.ReaderWriterLock>이 될 수 없는 경우  이 경우 컴파일러 오류가 발생 합니다.  
  
## <a name="example"></a>예제  
 이 예제에서는 여러 스레드에서 클래스의 단일 인스턴스를 사용 합니다.  클래스 자체에 잠금을 사용 하 여 내부 데이터에 대 한 액세스는 각 스레드에 대해 일치 되도록 합니다.  주 응용 프로그램 스레드는 주기적으로 확인 하는 경우 모든 작업자 스레드가 여전히 존재 하며 일까 지 모든 작업자 스레드가 끝나기를 대기 요소가 해당 작업을 완료 하는 클래스의 동일한 인스턴스에서 잠금을 사용 합니다.  
  
```  
// msl_lock_lock.cpp  
// compile with: /clr  
#include <msclr/lock.h>  
  
using namespace System;  
using namespace System::Threading;  
using namespace msclr;  
  
ref class CounterClass {  
private:  
   int Counter;     
  
public:  
   property int ThreadCount;  
  
   // function called by multiple threads, use lock to keep Counter consistent  
   // for each thread  
   void UseCounter() {  
      try {  
         lock l(this); // wait infinitely  
  
         Console::WriteLine("In thread {0}, Counter = {1}", Thread::CurrentThread->ManagedThreadId,   
            Counter);  
  
         for (int i = 0; i < 10; i++) {  
            Counter++;  
            Thread::Sleep(10);  
         }  
  
         Console::WriteLine("In thread {0}, Counter = {1}", Thread::CurrentThread->ManagedThreadId,   
            Counter);  
  
         Counter = 0;  
         // lock is automatically released when it goes out of scope and its destructor is called  
      }  
      catch (...) {  
         Console::WriteLine("Couldn't acquire lock!");  
      }  
  
      ThreadCount--;  
   }  
};  
  
int main() {  
   // create a few threads to contend for access to the shared data  
   CounterClass^ cc = gcnew CounterClass;  
   array<Thread^>^ tarr = gcnew array<Thread^>(5);  
   ThreadStart^ startDelegate = gcnew ThreadStart(cc, &CounterClass::UseCounter);  
   for (int i = 0; i < tarr->Length; i++) {  
      tarr[i] = gcnew Thread(startDelegate);  
      cc->ThreadCount++;  
      tarr[i]->Start();  
   }  
  
   // keep our main thread alive until all worker threads have completed  
   lock l(cc, lock_later); // don't lock now, just create the object  
   while (true) {  
      if (l.try_acquire(50)) { // try to acquire lock, don't throw an exception if can't  
         if (0 == cc->ThreadCount) {  
            Console::WriteLine("All threads completed.");  
            break; // all threads are gone, exit while  
         }  
         else {  
            Console::WriteLine("{0} threads exist, continue waiting...", cc->ThreadCount);  
            l.release(); // some threads exist, let them do their work  
         }  
      }  
   }  
}  
```  
  
```Output  
In thread 3, Counter = 0  
In thread 3, Counter = 10  
In thread 5, Counter = 0  
In thread 5, Counter = 10  
In thread 7, Counter = 0  
In thread 7, Counter = 10  
In thread 4, Counter = 0  
In thread 4, Counter = 10  
In thread 6, Counter = 0  
In thread 6, Counter = 10  
All threads completed.  
```  
  
## <a name="requirements"></a>요구 사항  
 **헤더 파일** \<msclr\lock.h >  
  
 **Namespace** msclr  
  
## <a name="see-also"></a>참고 항목  
 [lock 멤버](../dotnet/lock-members.md)   
 [잠금:: ~ 잠금](../dotnet/lock-tilde-lock.md)   
 [lock::acquire](../dotnet/lock-acquire.md)   
 [lock::try_acquire](../dotnet/lock-try-acquire.md)