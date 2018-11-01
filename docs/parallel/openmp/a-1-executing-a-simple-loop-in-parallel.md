---
title: A.1   병렬로 단일 루프 실행
ms.date: 11/04/2016
ms.assetid: b8aaacae-b20d-4b16-a540-54ccbf09582b
ms.openlocfilehash: 5bd9a9c8b1d226c67f7e9031a547e551fae3407b
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50558940"
---
# <a name="a1---executing-a-simple-loop-in-parallel"></a>A.1   병렬로 단일 루프 실행

다음 예제에서는 사용 하 여 간단한 루프를 병렬화 하는 방법에 설명 합니다 `parallel for` 지시문 ([2.5.1 섹션](../../parallel/openmp/2-5-1-parallel-for-construct.md) 16 페이지). 루프 반복 변수 기본적으로 비공개 이므로 개인 절에 명시적으로 지정할 필요는 없습니다.

```
#pragma omp parallel for
    for (i=1; i<n; i++)
        b[i] = (a[i] + a[i-1]) / 2.0;
```