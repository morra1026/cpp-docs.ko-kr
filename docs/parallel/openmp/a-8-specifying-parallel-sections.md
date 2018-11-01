---
title: A.8   Parallel Sections 지정
ms.date: 11/04/2016
ms.assetid: cf399304-121e-4c07-9829-47e0dbc2ef10
ms.openlocfilehash: 81eaed920e77b23052ac58c2d0e18fee83c00565
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50461440"
---
# <a name="a8---specifying-parallel-sections"></a>A.8   Parallel Sections 지정

다음 예에서 (에 대 한 [2.4.2 섹션](../../parallel/openmp/2-4-2-sections-construct.md) 14 페이지) 함수 *x 축*합니다 *yaxis*, 및 *zaxis* 동시에 실행할 수 있습니다. 첫 번째 `section` 지시문은 선택 사항입니다.  모든 `section` 지시문의 어휘 범위에 표시 되어야 합니다 `parallel sections` 생성 합니다.

```
#pragma omp parallel sections
{
    #pragma omp section
        xaxis();
    #pragma omp section
        yaxis();
    #pragma omp section
        zaxis();
}
```