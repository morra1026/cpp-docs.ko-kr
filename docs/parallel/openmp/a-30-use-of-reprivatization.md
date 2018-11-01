---
title: A.30   재전용화 사용
ms.date: 11/04/2016
ms.assetid: 26529090-6c39-40f2-b806-e12374d6b5f8
ms.openlocfilehash: dc1d142a282fe6bb55c9cc512e6a6e8155b286e4
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50437325"
---
# <a name="a30---use-of-reprivatization"></a>A.30   재전용화 사용

다음 예제에서는 변수의 재 전용 화는 방법을 보여 줍니다. Private 변수를 표시할 수 있습니다 `private` 중첩 된 지시문에서 다시 합니다. 병렬 영역 바깥쪽에서 공유 될 필요가 없습니다.

```
int i, a;
...
#pragma omp parallel private(a)
{
  ...
  #pragma omp parallel for private(a)
  for (i=0; i<10; i++)
     {
       ...
     }
}
```