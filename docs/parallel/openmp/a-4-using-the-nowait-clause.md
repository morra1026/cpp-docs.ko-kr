---
title: A.4 nowait 절 사용 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: d3de2111-05ea-4ee3-a66c-57bd988712af
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: da4b69ed8ccf59fb90d17da2b85d7693d661785b
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46444504"
---
# <a name="a4---using-the-nowait-clause"></a>A.4   nowait 절 사용

병렬 영역 내부에서는 여러 독립적인 루프의 경우 사용할 수는 `nowait` 절 ([2.4.1 섹션](../../parallel/openmp/2-4-1-for-construct.md) 11 페이지) 끝에 암시적된 장벽을 사용 하지 않으려면는 `for` 다음과 같은 지시문:

```
#pragma omp parallel
{
    #pragma omp for nowait
        for (i=1; i<n; i++)
             b[i] = (a[i] + a[i-1]) / 2.0;
    #pragma omp for nowait
        for (i=0; i<m; i++)
            y[i] = sqrt(z[i]);
}
```