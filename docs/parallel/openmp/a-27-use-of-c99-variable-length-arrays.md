---
title: A.27   C99 가변 길이 배열 사용
ms.date: 11/04/2016
ms.assetid: 8e542701-39f9-4f28-ab3a-840e8e669723
ms.openlocfilehash: 7b2ee74dcd5adedd02e7a9b311c5d3f67203d892
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50655301"
---
# <a name="a27---use-of-c99-variable-length-arrays"></a>A.27   C99 가변 길이 배열 사용

다음 예제에서 C99 가변 길이 배열 (Vla)를 사용 하는 방법에 설명 된 `firstprivate` 지시문 ([2.7.2.2 섹션](../../parallel/openmp/2-7-2-2-firstprivate.md) 26 페이지).

> [!NOTE]
>  Visual c + +에서 가변 길이 배열은 현재 지원 되지 않습니다.

```
void f(int m, int C[m][m])
{
    double v1[m];
    ...
    #pragma omp parallel firstprivate(C, v1)
    ...
}
```