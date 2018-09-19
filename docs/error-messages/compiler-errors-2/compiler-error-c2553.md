---
title: 컴파일러 오류 C2553 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2553
dev_langs:
- C++
helpviewer_keywords:
- C2553
ms.assetid: 64bc1e9a-627f-4ce9-b7bc-dc911bdb9180
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 38fb61b7281dd0371c546fd7b7bc960232cf2e00
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46043991"
---
# <a name="compiler-error-c2553"></a>컴파일러 오류 C2553

'base_function': 재정의 가상 함수의 반환 형식은 'override_function'에서 다릅니다.

파생된 클래스의 함수가 기본 클래스에서 가상 함수를 재정의 하려고 하지만 파생된 클래스는 기본 클래스 함수의 반환 형식이 없는 합니다.  함수 시그니처는 재정의 재정의 되는 함수의 시그니처와 일치 해야 합니다.

다음 샘플에서는 C2553 오류가 생성 됩니다.

```
// C2553.cpp
// compile with: /clr /c
ref struct C {
   virtual void f();
};

ref struct D : C {
   virtual int f() override ;   // C2553

   // try the following line instead
   // virtual void f() override;
};
```