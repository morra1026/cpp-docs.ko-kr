---
title: 컴파일러 경고(수준 1) C4384
ms.date: 11/04/2016
f1_keywords:
- C4384
helpviewer_keywords:
- C4384
ms.assetid: fafa8eb2-cbfc-4edb-8b0f-511ff5d37ac0
ms.openlocfilehash: 0f2666011e88dfd59eaaca154f4407bece7c963c
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50454691"
---
# <a name="compiler-warning-level-1-c4384"></a>컴파일러 경고(수준 1) C4384

\#pragma 'make_public' 전역 범위에만 사용할 수

합니다 [make_public](../../preprocessor/make-public.md) pragma 올바르게 적용 되었습니다.

## <a name="example"></a>예제

다음 샘플에서는 C4384 오류가 발생 합니다.

```
// C4384.cpp
// compile with: /c /W1
namespace n {
   #pragma make_public(N::C)   // C4384
   namespace N {
      class C {};
   }
}
```