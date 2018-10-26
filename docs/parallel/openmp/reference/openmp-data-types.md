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
ms.openlocfilehash: 97cf6ccad0a3b30c0abfa0076ea9c6a30b205d67
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50065202"
---
# <a name="openmp-data-types"></a>OpenMP 데이터 형식

OpenMP API에서 사용 되는 데이터 형식에 대 한 링크를 제공 합니다.

표준 OpenMP의 Visual c + + 구현에는 다음 데이터 형식 포함 됩니다.

|데이터 형식|설명|
|---------|-----------|
|[omp_lock_t](#omp-lock-t)|잠금, 잠금을 사용할 수 있는지 또는 스레드가 잠금을 소유 하는 경우의 상태를 보유 하는 형식입니다.|
|[omp_nest_lock_t](#omp-nest-lock-t)|잠금에 대 한 정보는 다음과 같은 부분 중 하나를 포함 하는 형식: 잠금을 사용할 수는 스레드의 id를 소유 하는 잠금 및 중첩 수 있는지 여부를 합니다.|

## <a name="omp-lock-t"></a>omp_lock_t

잠금, 잠금을 사용할 수 있는지 또는 스레드가 잠금을 소유 하는 경우의 상태를 보유 하는 형식입니다.

다음 함수는 사용 하 여 `omp_lock_t`:

- [omp_init_lock](openmp-functions.md#omp-init-lock)
- [omp_destroy_lock](openmp-functions.md#omp-destroy-lock)
- [omp_set_lock](openmp-functions.md#omp-set-lock)
- [omp_unset_lock](openmp-functions.md#omp-unset-lock)
- [omp_test_lock](openmp-functions.md#omp-test-lock)

자세한 내용은 [3.2 Lock 함수](../../../parallel/openmp/3-2-lock-functions.md)합니다.

### <a name="example"></a>예제

참조 [omp_init_lock](openmp-functions.md#omp-init-lock) 사용 하는 예제에 대 한 `omp_lock_t`합니다.

## <a name="omp-nest-lock-t"></a>omp_nest_lock_t

잠금에 대 한 정보는 다음 정보를 포함 하는 형식: 잠금을 사용할 수는 스레드의 id를 소유 하는 잠금 및 중첩 수 있는지 여부를 합니다.

다음 함수는 사용 하 여 `omp_nest_lock_t`:

- [omp_init_nest_lock](openmp-functions.md#omp-init-nest-lock)
- [omp_destroy_nest_lock](openmp-functions.md#omp-destroy-nest-lock)
- [omp_set_nest_lock](openmp-functions.md#omp-set-nest-lock)
- [omp_unset_nest_lock](openmp-functions.md#omp-unset-nest-lock)
- [omp_test_nest_lock](openmp-functions.md#omp-test-nest-lock)

자세한 내용은 [3.2 Lock 함수](../../../parallel/openmp/3-2-lock-functions.md)합니다.

### <a name="example"></a>예제

참조 [omp_init_nest_lock](openmp-functions.md#omp-init-nest-lock) 사용 하는 예제에 대 한 `omp_nest_lock_t`합니다.
