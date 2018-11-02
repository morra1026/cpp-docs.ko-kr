---
title: 컴파일러 오류 C3753
ms.date: 11/04/2016
f1_keywords:
- C3753
helpviewer_keywords:
- C3753
ms.assetid: a5b99e28-796c-4107-a673-97c2ae3bb2b9
ms.openlocfilehash: b6b1e8c3241a778b29045e734fffebb663554e62
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50498373"
---
# <a name="compiler-error-c3753"></a>컴파일러 오류 C3753

일반 속성이 허용 되지 않습니다.

제네릭 매개 변수 목록은 관리 되는 클래스, 구조체 또는 함수에만 나타날 수 있습니다.

자세한 내용은 [제네릭을](../../windows/generics-cpp-component-extensions.md) 하 고 [속성](../../windows/property-cpp-component-extensions.md)합니다.

## <a name="example"></a>예제

다음 샘플 C3753를 생성합니다.

```
// C3753.cpp
// compile with: /clr /c
ref struct A {
   generic <typename T>
   property int i;   // C3753 error
};
```