---
title: A.21   private 절을 사용하여 변수에 범위 지정
ms.date: 11/04/2016
ms.assetid: 7cdb4a7f-af24-44ac-9d33-e43840bc8f3d
ms.openlocfilehash: 4217bcc3911ded88b9385695c8c0ac851fceae9e
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50616130"
---
# <a name="a21---scoping-variables-with-the-private-clause"></a>A.21   private 절을 사용하여 변수에 범위 지정

값 `i` 고 `j` 다음 예제에서는 정의 되지 않은 병렬 영역에서 종료 시:

```
int i, j;
i = 1;
j = 2;
#pragma omp parallel private(i) firstprivate(j)
{
  i = 3;
  j = j + 2;
}
printf_s("%d %d\n", i, j);
```

대 한 자세한 내용은 합니다 `private` 절을 참조 하세요 [2.7.2.1 섹션](../../parallel/openmp/2-7-2-1-private.md) 25 페이지입니다.