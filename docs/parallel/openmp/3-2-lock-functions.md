---
title: 3.2 함수 잠금 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 0ec855c6-55a9-49d7-bee4-5edae6e86a1b
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 97f125129d4b35586111f3d4092d457560aaebec
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46412277"
---
# <a name="32-lock-functions"></a>3.2 Lock 함수

이 섹션에 설명 된 함수에는 동기화에 사용 되는 잠금 조작 합니다.

다음 함수에 대 한 잠금 변수의 형식이 있어야 **omp_lock_t**합니다. 이 변수는 이러한 함수를 통해만 액세스 해야 합니다. 모든 잠금 함수에 대 한 포인터를 인수로 필요 **omp_lock_t** 형식입니다.

- `omp_init_lock` 함수 간단한 잠금을 초기화 합니다.

- `omp_destroy_lock` 함수는 간단한 잠금을 제거 합니다.

- `omp_set_lock` 함수 간단한 잠금 제공 될 때까지 대기 합니다.

- `omp_unset_lock` 함수에는 간단한 잠금을 해제 합니다.

- `omp_test_lock` 함수 간단한 잠금 테스트 합니다.

다음 함수에 대 한 잠금 변수의 형식이 있어야 **omp_nest_lock_t**합니다.  이 변수는 이러한 함수를 통해만 액세스 해야 합니다. 모든 중첩 가능 잠금을 함수에 대 한 포인터를 인수로 필요 **omp_nest_lock_t** 형식입니다.

- `omp_init_nest_lock` 함수를 중첩 가능 잠금을 초기화 합니다.

- `omp_destroy_nest_lock` 함수를 중첩 가능 잠금을 제거 합니다.

- `omp_set_nest_lock` 함수를 중첩 가능 잠금 사용 가능할 때까지 대기 합니다.

- `omp_unset_nest_lock` 함수 중첩 가능 잠금을 해제 합니다.

- `omp_test_nest_lock` 함수를 중첩 가능 잠금 테스트 합니다.

OpenMP lock 함수에는 항상 읽기 하며 최신 잠금 변수의 값을 업데이트 하는 방식으로 잠금을 변수에 액세스 합니다. 명시적으로 포함 하는 OpenMP 프로그램에 대 한 필요 없는 따라서 **플러시** 지시문을 잠금 변수의 값이 다른 스레드 간에 일치 하는지 확인 합니다. (에 대 한 요구가 있을 **플러시** 지시문을 다른 변수 값을 일관 되 게 합니다.)