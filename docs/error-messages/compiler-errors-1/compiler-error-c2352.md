---
title: 컴파일러 오류 C2352 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2352
dev_langs:
- C++
helpviewer_keywords:
- C2352
ms.assetid: 0efad8cb-659f-4b3e-8f6f-9f8ec44d345c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 29e1c63486c26a2f2ef34dbb1165c581a0c074cd
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46060254"
---
# <a name="compiler-error-c2352"></a>컴파일러 오류 C2352

'class::function': 비정적 멤버 함수를 잘못 호출했습니다.

`static` 멤버 함수가 비정적 멤버 함수를 호출했습니다. 또는 비정적 멤버 함수가 클래스 외부에서 정적 함수로 호출되었습니다.

다음 샘플에서는 C2352를 생성하고 해결 방법을 보여 줍니다.

```
// C2352.cpp
// compile with: /c
class CMyClass {
public:
   static void func1();
   void func2();
   static void func3() {
      func2();   // C2352 calls nonstatic func2
      func1();   // OK calls static func1
   }
};
```

다음 샘플에서는 C2352를 생성하고 해결 방법을 보여 줍니다.

```
// C2352b.cpp
class MyClass {
public:
   void MyFunc() {}
   static void MyFunc2() {}
};

int main() {
   MyClass::MyFunc();   // C2352
   MyClass::MyFunc2();   // OK
}
```