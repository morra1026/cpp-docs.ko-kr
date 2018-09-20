---
title: A.15 사용 되는 스레드 수를 결정 합니다. | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 026bb59a-f668-40db-a7cb-69a1bae83d2d
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 1042b4871f53bddb5cff894330f3afe7d8a088ef
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46428743"
---
# <a name="a15---determining-the-number-of-threads-used"></a>A.15   사용된 스레드 수 확인

다음 예제에서는 잘못 된 것이 좋습니다 (에 대 한 [단원 3.1.2](../../parallel/openmp/3-1-2-omp-get-num-threads-function.md) 37 페이지):

```
np = omp_get_num_threads(); // misplaced
#pragma omp parallel for schedule(static)
    for (i=0; i<np; i++)
        work(i);
```

`omp_get_num_threads()` 하므로 코드의 직렬 섹션에서 1을 반환 호출 *np* 항상 앞의 예제에서 1와 같게 됩니다. 병렬 영역에 대 한 배포 될 스레드의 수를 확인 하려면 병렬 영역 내에서 호출 해야 합니다.

다음 예제에서는 스레드 수에 대 한 쿼리를 포함 하지 않고이 프로그램을 다시 작성 하는 방법을 보여 줍니다.

```
#pragma omp parallel private(i)
{
    i = omp_get_thread_num();
    work(i);
}
```