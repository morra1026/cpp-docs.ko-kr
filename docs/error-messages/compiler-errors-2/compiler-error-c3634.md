---
title: 컴파일러 오류 C3634 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3634
dev_langs:
- C++
helpviewer_keywords:
- C3634
ms.assetid: fd09f10c-f863-483b-9756-71c16b760b02
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d3a8ef6c2b1f57e09a62e8f08efc2a4cc1f6e2e3
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46110577"
---
# <a name="compiler-error-c3634"></a>컴파일러 오류 C3634

'function': 관리 되는 또는 WinRTclass 추상 메서드를 정의할 수 없습니다.

WinRT 또는 관리되는 클래스에서 추상 메서드를 선언할 수 있지만 정의할 수는 없습니다.

## <a name="example"></a>예제

다음 샘플에서는 C3634 오류가 발생하는 경우를 보여 줍니다.

```
// C3634.cpp
// compile with: /clr
ref class C {
   virtual void f() = 0;
};

void C::f() {   // C3634 - don't define managed class' pure virtual method
}
```
