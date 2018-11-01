---
title: 컴파일러 오류 C2201
ms.date: 11/04/2016
f1_keywords:
- C2201
helpviewer_keywords:
- C2201
ms.assetid: ed927659-6e9c-447d-9963-19969ae1e957
ms.openlocfilehash: b011c5027af6c0561010c6d11d3efd07234549f3
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50621601"
---
# <a name="compiler-error-c2201"></a>컴파일러 오류 C2201

'identifier': 외부 링크가 내보내고 가져올 수 있어야 합니다

내보낸된 식별자는 `static`합니다.

다음 샘플에서는 C2286을 생성합니다.

```
// C2201.cpp
// compile with: /c
__declspec(dllexport) static void func() {}   // C2201 func() is static
__declspec(dllexport) void func2() {}   // OK
```

## <a name="see-also"></a>참고 항목

[링크 형식](../../cpp/types-of-linkage.md)