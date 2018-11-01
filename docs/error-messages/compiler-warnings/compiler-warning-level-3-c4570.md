---
title: 컴파일러 경고(수준 3) C4570
ms.date: 11/04/2016
f1_keywords:
- C4570
helpviewer_keywords:
- C4570
ms.assetid: feec1225-e6ad-4995-8d96-c22e864a77bd
ms.openlocfilehash: 1c92bd7f632ea6662c3cee1bcaa1dd0c917fb2a1
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50661307"
---
# <a name="compiler-warning-level-3-c4570"></a>컴파일러 경고(수준 3) C4570

'type': 명시적으로 선언 되지 추상 않았지만 추상 함수를가지고

포함 하는 형식을 [추상](../../windows/abstract-cpp-component-extensions.md) 함수 자체 될 추상으로 표시 되어야 합니다.

## <a name="example"></a>예제

다음 샘플에서는 C4570 오류가 발생 합니다.

```
// C4570.cpp
// compile with: /clr /W3 /c
ref struct X {   // C4570
// try the following line instead
// ref class X abstract {
   virtual void f() abstract;
};
```