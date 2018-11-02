---
title: 컴파일러 오류 C2776
ms.date: 11/04/2016
f1_keywords:
- C2776
helpviewer_keywords:
- C2776
ms.assetid: 9d80addc-62c7-40fc-a2cc-60303abb87df
ms.openlocfilehash: 200fbc5c42a6b735c072c093ec4cb4f081031824
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50652145"
---
# <a name="compiler-error-c2776"></a>컴파일러 오류 C2776

속성 당 'get' 메서드 하나만 지정할 수 있습니다.

만 지정할 수 있습니다 `get` 함수는 [속성](../../cpp/property-cpp.md) 확장 된 특성입니다. 이 오류가 발생할 때 여러 `get` 함수가 지정 됩니다.

다음 샘플에서는 C2776 오류가 생성 됩니다.

```
// C2776.cpp
struct A {
   __declspec(property(get=GetProp,get=GetPropToo))
   // try the following line instead
   // __declspec(property(get=GetProp))
      int prop;   // C2776
   int GetProp(void);
   int GetPropToo(void);
};
```