---
title: A.24 private 절 예제 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: f90a5b49-81ff-4746-ae03-37bbd33f6c08
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: df2efc9fe111fa6e8d0b0507eceb20f07f48b02d
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46416242"
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