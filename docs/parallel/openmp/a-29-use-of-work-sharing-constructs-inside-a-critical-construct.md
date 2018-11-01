---
title: A.29   critical 구문 내 작업 공유 구문 사용
ms.date: 11/04/2016
ms.assetid: d5c8a83f-2f51-4f23-8ddf-d267e347507f
ms.openlocfilehash: fac5576f859f63298d658b51c4307bb238e301c8
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50643588"
---
# <a name="a29---use-of-work-sharing-constructs-inside-a-critical-construct"></a>A.29   critical 구문 내 작업 공유 구문 사용

다음 예제에서는 내 작업 공유 구문을 사용 하는 `critical` 생성 합니다. 이 예제는 규격 상태가 생성 작업 공유 및 `critical` 구문을 병렬 동일한 지역에 바인딩하지 마십시오.

```
void f()
{
  int i = 1;
  #pragma omp parallel sections
  {
    #pragma omp section
    {
      #pragma omp critical (name)
      {
        #pragma omp parallel
        {
          #pragma omp single
          {
            i++;
          }
        }
      }
    }
  }
}
```