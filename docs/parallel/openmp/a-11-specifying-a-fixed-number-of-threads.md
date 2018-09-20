---
title: A.11 고정된 된 수의 스레드를 지정 합니다. | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 1d06b142-4c35-44b8-994b-20f2aed5462b
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 892140425dc9f7083c606fce3ffe671a107a65ca
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46422989"
---
# <a name="a11---specifying-a-fixed-number-of-threads"></a>A.11   고정된 수의 스레드 지정

일부 프로그램 고정, 미리 지정한 수의 스레드를 정확 하 게 실행을 사용 합니다.  구현 시 정의 된 스레드 수를 동적으로 조정 해야 하는 항목에 대 한 기본 설정 이기 때문에 이러한 프로그램 동적 스레드는 기능을 해제 하 고 이식성을 보장 하는 명시적으로 스레드 수를 설정할 수 있습니다. 다음 예제에서는 사용 하는 방법을 보여 줍니다 `omp_set_dynamic` ([3.1.7 섹션](../../parallel/openmp/3-1-7-omp-set-dynamic-function.md) 39 페이지), 및 `omp_set_num_threads` ([3.1.1 섹션](../../parallel/openmp/3-1-1-omp-set-num-threads-function.md) 36 페이지):

```
omp_set_dynamic(0);
omp_set_num_threads(16);
#pragma omp parallel shared(x, npoints) private(iam, ipoints)
{
    if (omp_get_num_threads() != 16)
      abort();
    iam = omp_get_thread_num();
    ipoints = npoints/16;
    do_by_16(x, iam, ipoints);
}
```

이 예제에서는 프로그램 16 스레드에 의해 실행 된 경우에 올바르게를 실행 합니다. 구현 스레드는 16을 지원할 수 없는 경우이 예의 동작은 구현 시 정의입니다.

동적 스레드 설정에 관계 없이 병렬 영역, 병렬 영역을 실행 하는 스레드 수가 동안 상수는 참고 합니다. 병렬 영역의 시작 부분에 사용할 스레드 수를 결정 하 고 지역 기간에 대 한 상수 유지 하는 동적 스레드 메커니즘을 합니다.