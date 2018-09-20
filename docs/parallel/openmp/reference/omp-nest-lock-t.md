---
title: omp_nest_lock_t | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
f1_keywords:
- omp_nest_lock_t
dev_langs:
- C++
helpviewer_keywords:
- omp_nest_lock_t OpenMP data type
ms.assetid: fceac9fb-96d2-42b0-af19-c9b078380618
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: b25a76332325247987751d8e9c41914da51f4a70
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46390138"
---
# <a name="ompnestlockt"></a>omp_nest_lock_t

잠금에 대 한 정보는 다음 정보를 포함 하는 형식: 잠금을 사용할 수는 스레드의 id를 소유 하는 잠금 및 중첩 수 있는지 여부를 합니다.

다음 함수는 사용 하 여 **omp_nest_lock_t**:

- [omp_init_nest_lock](../../../parallel/openmp/reference/omp-init-nest-lock.md)

- [omp_destroy_nest_lock](../../../parallel/openmp/reference/omp-destroy-nest-lock.md)

- [omp_set_nest_lock](../../../parallel/openmp/reference/omp-set-nest-lock.md)

- [omp_unset_nest_lock](../../../parallel/openmp/reference/omp-unset-nest-lock.md)

- [omp_test_nest_lock](../../../parallel/openmp/reference/omp-test-nest-lock.md)

자세한 내용은 [3.2 Lock 함수](../../../parallel/openmp/3-2-lock-functions.md)합니다.

## <a name="example"></a>예제

참조 [omp_init_nest_lock](../../../parallel/openmp/reference/omp-init-nest-lock.md) 사용 하는 예제에 대 한 **omp_nest_lock_t**합니다.

## <a name="see-also"></a>참고 항목

[데이터 형식](../../../parallel/openmp/reference/openmp-data-types.md)