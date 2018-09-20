---
title: A.26 threadprivate 지시문 사용 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 6eda76c2-c4f1-4208-a900-e0ea98a53eca
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 93a596a4015f92e2a4d42151560171157232047b
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46447652"
---
# <a name="a26---using-the-threadprivate-directive"></a>A.26   threadprivate 지시문 사용

다음 예제에 사용 하는 방법을 보여 줍니다 합니다 `threadprivate` 지시문 ([2.7.1 섹션](../../parallel/openmp/2-7-1-threadprivate-directive.md) 23 페이지) 각 스레드에 별도 카운터를 제공 합니다.

**예제 1:**

```
int counter = 0;
#pragma omp threadprivate(counter)

int sub()
{
    counter++;
    return(counter);
}
```

**예제 2:**

```
int sub()
{
    static int counter = 0;
    #pragma omp threadprivate(counter)
    counter++;
    return(counter);
}
```