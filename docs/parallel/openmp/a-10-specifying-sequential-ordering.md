---
title: A.10 순차적 정렬 지정 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 5c65a9b1-0fc5-4cad-a5a9-9ce10b25d25c
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 29f2089760e9aef6f9e992c5725eab12b7be3b20
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46432232"
---
# <a name="a10---specifying-sequential-ordering"></a>A.10   순차적 정렬 지정

정렬 섹션 ([2.6.6 섹션](../../parallel/openmp/2-6-6-ordered-construct.md) 22 페이지) 순차적으로 병렬로 수행 되는 작업의 출력을 정렬 하는 데 유용 합니다. 다음 프로그램 순차적에서 인덱스를 출력 합니다.

```
#pragma omp for ordered schedule(dynamic)
    for (i=lb; i<ub; i+=st)
        work(i);
void work(int k)
{
    #pragma omp ordered
        printf_s(" %d", k);
}
```