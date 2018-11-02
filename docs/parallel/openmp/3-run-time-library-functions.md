---
title: 3. 런타임 라이브러리 함수
ms.date: 11/04/2016
ms.assetid: b226e512-6822-4cbe-a2ca-74cc2bb7e880
ms.openlocfilehash: e1d8d498be7f58bcf510025c67c539127f450824
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50484099"
---
# <a name="3-run-time-library-functions"></a>3. 런타임 라이브러리 함수

이 섹션에는 OpenMP C 및 c + + 런타임 라이브러리 함수를 설명합니다. 헤더  **\<omp.h >** 두 형식, 제어 및 병렬 실행 환경으로 쿼리 및 데이터에 대 한 액세스를 동기화 하는 함수를 잠글 수 있는 몇 가지 함수를 선언 합니다.

형식 **omp_lock_t** 잠금 수를 표현할 수 있는 되지 않는 개체 유형 또는 스레드가 잠금을 소유 하 고 있습니다. 이러한 잠금은 이라고 *간단한 잠금을*합니다.

형식 **omp_nest_lock_t** 는 것을 표현할 수 있는 개체 형식의 잠금을 사용 가능 하거나 잠금을 소유 하는 스레드의 id 및 *개수 중첩* (아래 설명 참조). 이러한 잠금은 이라고 *중첩 가능 잠금*합니다.

라이브러리 함수는 "C" 링크를 사용 하 여 외부 함수입니다.

이 챕터의 설명에 다음 항목으로 나뉩니다.

- 실행 환경 함수 (참조 [섹션 3.1](../../parallel/openmp/3-1-execution-environment-functions.md) 35 페이지).

- 함수 잠금 (참조 [섹션 3.2](../../parallel/openmp/3-2-lock-functions.md) 41 페이지).