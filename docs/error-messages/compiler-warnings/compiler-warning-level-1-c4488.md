---
title: 컴파일러 경고 (수준 1) C4488 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4488
dev_langs:
- C++
helpviewer_keywords:
- C4488
ms.assetid: 55625e46-ddb5-4c7c-99c7-cd4aa9f879bd
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 0d2cccedada47519ada55353cb44faab0e34cf03
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46118273"
---
# <a name="compiler-warning-level-1-c4488"></a>컴파일러 경고(수준 1) C4488

'function': 인터페이스 메서드 'interface_method'를 구현 하는 'keyword' 키워드를 필요

클래스는 자신이 직접 상속 된 인터페이스의 모든 멤버를 구현 해야 합니다. 구현 된 멤버를 public 액세스 가능성이 있어야 및 virtual로 표시할 수 있습니다.

## <a name="example"></a>예제

구현 된 멤버를 public이 아닙니다 C4488 발생할 수 있습니다. 다음 샘플 C4488를 생성합니다.

```
// C4488.cpp
// compile with: /clr /c /W1 /WX
interface struct MyI {
   void f1();
};

// implemented member not public
ref class B : MyI { virtual void f1() {} };  // C4488

// OK
ref class C : MyI {
public:
   virtual void f1() {}
};
```

## <a name="example"></a>예제

구현 된 멤버를 가상 표시 되지 않으면 C4488 발생할 수 있습니다. 다음 샘플 C4488를 생성합니다.

```
// C4488_b.cpp
// compile with: /clr /c /W1 /WX
interface struct MyI {
   void f1();
};

ref struct B : MyI { void f1() {} };   // C4488
ref struct C : MyI { virtual void f1() {} };   // OK
```