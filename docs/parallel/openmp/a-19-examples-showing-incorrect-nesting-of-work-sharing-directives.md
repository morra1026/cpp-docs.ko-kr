---
title: A.19   작업 공유 지시문의 잘못된 중첩을 보여 주는 예제
ms.date: 11/04/2016
ms.assetid: 906e900d-9259-44d6-a095-c1ba9135d269
ms.openlocfilehash: 5be09dd3282260dabc2ef30dafc249539d6a6418
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50501948"
---
# <a name="a19---examples-showing-incorrect-nesting-of-work-sharing-directives"></a>A.19   작업 공유 지시문의 잘못된 중첩을 보여 주는 예제

이 섹션의 예제에서는 지시문 중첩 규칙을 보여 줍니다. 지시문 중첩에 대 한 자세한 내용은 참조 하세요. [2.9 섹션](../../parallel/openmp/2-9-directive-nesting.md) 33 페이지입니다.

다음 예제는 비규격 때문에 내부 및 외부 `for` 지시문은 중첩 되어 있고 동일한 바인딩 `parallel` 지시문:

```
void wrong1(int n)
{
  #pragma omp parallel default(shared)
  {
      int i, j;
      #pragma omp for
      for (i=0; i<n; i++) {
          #pragma omp for
              for (j=0; j<n; j++)
                 work(i, j);
     }
   }
}
```

위 예의 동적으로 중첩 된 다음 버전 비규격 이기도합니다.

```
void wrong2(int n)
{
  #pragma omp parallel default(shared)
  {
    int i;
    #pragma omp for
      for (i=0; i<n; i++)
        work1(i, n);
  }
}

void work1(int i, int n)
{
  int j;
  #pragma omp for
    for (j=0; j<n; j++)
      work2(i, j);
}
```

다음 예제는 비규격 때문에 합니다 `for` 및 `single` 지시문 중첩 되어 있고 동일한 병렬 영역을 바인딩할 때:

```
void wrong3(int n)
{
  #pragma omp parallel default(shared)
  {
    int i;
    #pragma omp for
      for (i=0; i<n; i++) {
        #pragma omp single
          work(i);
      }
  }
}
```

다음 예제는 비규격 때문에 `barrier` 내에서 지시문을 `for` 교착 상태가 발생할 수 있습니다:

```
void wrong4(int n)
{
  #pragma omp parallel default(shared)
  {
    int i;
    #pragma omp for
      for (i=0; i<n; i++) {
        work1(i);
        #pragma omp barrier
        work2(i);
      }
  }
}
```

다음 예제는 비규격 때문에 `barrier` 때문에 한 번에 하나의 스레드만 중요 섹션에 입력할 수 교착 상태에서 결과:

```
void wrong5()
{
  #pragma omp parallel
  {
    #pragma omp critical
    {
       work1();
       #pragma omp barrier
       work2();
    }
  }
}
```

다음 예제는 비규격 때문에 합니다 `barrier` 때문에 하나의 스레드만 실행 교착 상태에서 결과 `single` 섹션:

```
void wrong6()
{
  #pragma omp parallel
  {
    setup();
    #pragma omp single
    {
      work1();
      #pragma omp barrier
      work2();
    }
    finish();
  }
}
```