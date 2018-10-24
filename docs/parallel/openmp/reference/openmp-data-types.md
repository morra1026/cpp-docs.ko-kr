---
title: OpenMP 데이터 형식 | Microsoft Docs
ms.custom: ''
ms.date: 10/23/2018
ms.technology:
- cpp-parallel
ms.topic: reference
f1_keywords:
- OpenMP data types
- omp_lock_t
- omp_nest_lock_t
dev_langs:
- C++
helpviewer_keywords:
- OpenMP data types
- omp_lock_t OpenMP data type
- omp_nest_lock_t OpenMP data type
ms.assetid: cf1e1045-4d12-4d03-80b7-d5843b80ef85
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 254dffebc258867088f738b10a11bf48d31bd0a4
ms.sourcegitcommit: c045c3a7e9f2c7e3e0de5b7f9513e41d8b6d19b2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/24/2018
ms.locfileid: "49990071"
---
# <a name="openmp-data-types"></a>OpenMP 데이터 형식

OpenMP API에서 사용 되는 데이터 형식에 대 한 링크를 제공 합니다.

표준 OpenMP의 Visual c + + 구현에는 다음 데이터 형식 포함 됩니다.

데이터 형식                           | 설명
----------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
[omp_lock_t](#omp-lock-t)           | 잠금, 잠금을 사용할 수 있는지 또는 스레드가 잠금을 소유 하는 경우의 상태를 보유 하는 형식입니다.
[omp_nest_lock_t](#omp-nest-lock-t) | 잠금에 대 한 정보는 다음과 같은 부분 중 하나를 포함 하는 형식: 잠금을 사용할 수는 스레드의 id를 소유 하는 잠금 및 중첩 수 있는지 여부를 합니다.

## <a name="omp-lock-t"></a>omp_lock_t

잠금, 잠금을 사용할 수 있는지 또는 스레드가 잠금을 소유 하는 경우의 상태를 보유 하는 형식입니다.

다음 함수는 사용 하 여 `omp_lock_t`:

- [omp_init_lock](../../../parallel/openmp/reference/omp-init-lock.md)
- [omp_destroy_lock](../../../parallel/openmp/reference/omp-destroy-lock.md)
- [omp_set_lock](../../../parallel/openmp/reference/omp-set-lock.md)
- [omp_unset_lock](../../../parallel/openmp/reference/omp-unset-lock.md)
- [omp_test_lock](../../../parallel/openmp/reference/omp-test-lock.md)

자세한 내용은 [3.2 Lock 함수](../../../parallel/openmp/3-2-lock-functions.md)합니다.

### <a name="example"></a>예제

참조 [omp_init_lock](../../../parallel/openmp/reference/omp-init-lock.md) 사용 하는 예제에 대 한 `omp_lock_t`합니다.

## <a name="omp-nest-lock-t"></a>omp_nest_lock_t

잠금에 대 한 정보는 다음 정보를 포함 하는 형식: 잠금을 사용할 수는 스레드의 id를 소유 하는 잠금 및 중첩 수 있는지 여부를 합니다.

다음 함수는 사용 하 여 `omp_nest_lock_t`:

- [omp_init_nest_lock](../../../parallel/openmp/reference/omp-init-nest-lock.md)
- [omp_destroy_nest_lock](../../../parallel/openmp/reference/omp-destroy-nest-lock.md)
- [omp_set_nest_lock](../../../parallel/openmp/reference/omp-set-nest-lock.md)
- [omp_unset_nest_lock](../../../parallel/openmp/reference/omp-unset-nest-lock.md)
- [omp_test_nest_lock](../../../parallel/openmp/reference/omp-test-nest-lock.md)

자세한 내용은 [3.2 Lock 함수](../../../parallel/openmp/3-2-lock-functions.md)합니다.

### <a name="example"></a>예제

참조 [omp_init_nest_lock](../../../parallel/openmp/reference/omp-init-nest-lock.md) 사용 하는 예제에 대 한 `omp_nest_lock_t`합니다.
