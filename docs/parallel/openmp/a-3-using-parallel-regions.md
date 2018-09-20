---
title: A.3 병렬 영역 사용 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 575216a1-960a-47f7-9c82-7f660291fcfe
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 82bc1655584af300cb2d36a62250595839d74551
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46413083"
---
# <a name="a3---using-parallel-regions"></a>A.3   병렬 영역 사용

합니다 `parallel` 지시문 ([섹션 2.3](../../parallel/openmp/2-3-parallel-construct.md) 8 페이지) 조립 (coarse-grain) 병렬 프로그램에서 사용할 수 있습니다. 병렬 영역에서 각 스레드를 다음 예에서 전역 배열의 부분을 결정 `x` 작업할 스레드 수를 기준으로 합니다.

```
#pragma omp parallel shared(x, npoints) private(iam, np, ipoints)
{
    iam = omp_get_thread_num();
    np =  omp_get_num_threads();
    ipoints = npoints / np;
    subdomain(x, iam, ipoints);
}
```