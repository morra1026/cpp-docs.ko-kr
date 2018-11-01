---
title: 컴파일러 오류 C2495
ms.date: 11/04/2016
f1_keywords:
- C2495
helpviewer_keywords:
- C2495
ms.assetid: bb7066fe-3549-4901-97e4-157f3c04dd57
ms.openlocfilehash: 83a0359fce175b12dd18e2500d63d7a86bed9f0b
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50436038"
---
# <a name="compiler-error-c2495"></a>컴파일러 오류 C2495

'identifier': 'nothrow'는 함수 선언 또는 정의에 적용 될 수 있습니다

합니다 [nothrow](../../cpp/nothrow-cpp.md) 함수 선언 또는 정의에 확장 된 특성을 적용할 수 있습니다.

다음 샘플에서는 C2495 오류가 생성 됩니다.

```
// C2495.cpp
// compile with: /c
__declspec(nothrow) class X {   // C2495
   int m_data;
} x;

__declspec(nothrow) void test();   // OK
```