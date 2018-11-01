---
title: lock::~lock
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- ~lock
- msclr.lock.~lock
- lock.~lock
- msclr::lock::~lock
- lock::~lock
helpviewer_keywords:
- ~lock destructor
ms.assetid: 55fa9f6c-d7a6-48ef-9236-ee03342c1d20
ms.openlocfilehash: a545cf6a60b6eb52df416d89308719b67f041f29
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50575268"
---
# <a name="locklock"></a>lock::~lock

소멸을 `lock` 개체입니다.

## <a name="syntax"></a>구문

```
~lock();
```

## <a name="remarks"></a>설명

소멸자 호출 [lock::release](../dotnet/lock-release.md)합니다.

## <a name="example"></a>예제

이 예제에서는 여러 스레드에서 클래스의 단일 인스턴스를 사용 합니다.  클래스 자체에 잠금을 사용 하 여 내부 데이터에 대 한 액세스는 각 스레드에 대해 일치 되도록 합니다.  주 응용 프로그램 스레드는 주기적으로 확인 하는 경우 모든 작업자 스레드가 여전히 존재 하며 일까 지 모든 작업자 스레드가 끝나기를 대기 요소가 해당 작업을 완료 하는 클래스의 동일한 인스턴스에서 잠금을 사용 합니다.

```
// msl_lock_dtor.cpp
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

[lock 멤버](../dotnet/lock-members.md)<br/>
[lock::lock](../dotnet/lock-lock.md)