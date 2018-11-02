---
title: A.24   private 절 예제
ms.date: 11/04/2016
ms.assetid: f90a5b49-81ff-4746-ae03-37bbd33f6c08
ms.openlocfilehash: facf5b953b26d284f6bfed4f35a9162f6d2bf212
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50552960"
---
# <a name="a24---example-of-the-private-clause"></a>A.24   private 절 예제

합니다 `private` 절 ([2.7.2.1 섹션](../../parallel/openmp/2-7-2-1-private.md) 25 페이지)에 적용 영역의 동적 범위 아닌 어휘 범위의 지역에 병렬 영역입니다.  사용 하 여, 모든 변수의 예와 따라서 *는* 내에서 `for` 루틴에 루프 *f* 의 전용 복사본을 가리킵니다 *는*에서 사용 하는 동안 루틴 *g* 전역 가리킵니다 *는*합니다.

```
int a;

void f(int n)
{
    a = 0;

    #pragma omp parallel for private(a)
    for (int i=1; i<n; i++)
    {
        a = i;
        g(i, n);
        d(a);     // Private copy of "a"
        ...
    }
    ...

void g(int k, int n)
{
    h(k,a); // The global "a", not the private "a" in f
}
```