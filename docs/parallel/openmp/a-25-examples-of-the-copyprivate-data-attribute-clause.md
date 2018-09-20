---
title: A.25 copyprivate 데이터 특성 절 예제 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 7b1cb6a5-5691-4b95-b3ac-d7543ede6405
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 95d68c445c1c20e97725d869061027a9712c2462
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46413644"
---
# <a name="a25---examples-of-the-copyprivate-data-attribute-clause"></a>A.25   copyprivate 데이터 특성 절 예제

**예제 1:** 는 `copyprivate` 절 ([2.7.2.8 섹션](../../parallel/openmp/2-7-2-8-copyprivate.md) 32 페이지) 브로드캐스트를 다른 스레드에서 개인 변수의 모든 인스턴스에 직접 단일 스레드에 의해 획득 되는 값을 사용할 수 있습니다.

```
float x, y;
#pragma omp threadprivate(x, y)

void init( )
{
    float a;
    float b;

    #pragma omp single copyprivate(a,b,x,y)
    {
        get_values(a,b,x,y);
    }

    use_values(a, b, x, y);
}
```

경우 일상적인 *init* 라고 직렬 지역에서 해당 동작에서 영향을 받지 지시문의 현재 상태입니다. 호출한 후 합니다 *get_values* 루틴 한 스레드에 의해 실행 된, 스레드가 없는 개인 개체에서 지정 될 때까지 구문을 유지 *는*, *b*, *x*, 및 *y* 읽은 값을 사용 하 여 모든 스레드에서 정의 됩니다.

**예제 2:** 이전 예제와 달리 읽기 마스터 스레드 예를 들어, 특정 스레드에서 수행 해야 한다고 가정 합니다. 이 경우에 `copyprivate` 브로드캐스트를 직접 할 절을 사용할 수 없습니다 하지만 임시 공유 개체에 대 한 액세스를 위해 사용할 수 있습니다.

```
float read_next( )
{
    float * tmp;
    float return_val;

    #pragma omp single copyprivate(tmp)
    {
        tmp = (float *) malloc(sizeof(float));
    }

    #pragma omp master
    {
        get_float( tmp );
    }

    #pragma omp barrier
    return_val = *tmp;
    #pragma omp barrier

    #pragma omp single
    {
       free(tmp);
    }

    return return_val;
}
```

**예제 3:** 병렬 영역 내부에서는 필요한 잠금 개체의 수에 입력 하기 전에 쉽게 확인할 수 없으므로 가정 합니다. `copyprivate` 병렬 해당 영역 내에서 할당 된 공유 잠금 개체에 대 한 액세스를 제공 하려면 절을 사용할 수 있습니다.

```
#include <omp.h>

omp_lock_t *new_lock()
{
    omp_lock_t *lock_ptr;

    #pragma omp single copyprivate(lock_ptr)
    {
        lock_ptr = (omp_lock_t *) malloc(sizeof(omp_lock_t));
        omp_init_lock( lock_ptr );
    }

    return lock_ptr;
}
```