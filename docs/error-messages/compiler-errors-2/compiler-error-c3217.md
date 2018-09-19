---
title: 컴파일러 오류 C3217 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3217
dev_langs:
- C++
helpviewer_keywords:
- C3217
ms.assetid: 99070417-c23a-4d82-bdd2-04be1a07adea
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c407e8f77990bdbeea143c252a27292ac282497e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46063491"
---
# <a name="compiler-error-c3217"></a>컴파일러 오류 C3217

'param': 제네릭 매개 변수는 이 선언에서 제약을 받을 수 없습니다.

제약 조건의 형식이 잘못되었습니다. 제약 조건 제네릭 매개 변수는 제네릭 클래스 템플릿 매개 변수와 일치해야 합니다.

다음 샘플에서는 C3217을 생성합니다.

```
// C3217.cpp
// compile with: /clr
interface struct A {};

generic <class T>
ref class C {
   generic <class T1>
   where T : A   // C3217
   void f();
};
```

다음 샘플에는 가능한 해결 방법을 보여 줍니다.

```
// C3217b.cpp
// compile with: /clr /c
interface struct A {};

generic <class T>
ref class C {
   generic <class T1>
   where T1 : A
   void f();
};
```