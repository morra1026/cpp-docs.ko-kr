---
title: OpenMP 절 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
dev_langs:
- C++
ms.assetid: 806e7d8f-b204-4e4c-a12c-273ab540a7ca
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: afd0a8f66f9b0d027671629998597955b3aa69e9
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46378336"
---
# <a name="openmp-clauses"></a>OpenMP 절

OpenMP API에서 사용 하는 절에 대 한 링크를 제공 합니다.

Visual c + +에서는 다음 OpenMP 절을 지원합니다.

|절|설명|
|------------|-----------------|
|[copyin](../../../parallel/openmp/reference/copyin.md)|스레드가 마스터 스레드에 값에 대 한 액세스 하도록 허용 된 [threadprivate](../../../parallel/openmp/reference/threadprivate.md) 변수입니다.|
|[copyprivate](../../../parallel/openmp/reference/copyprivate.md)|하나 이상의 변수는 모든 스레드 간에 공유 해야 지정 합니다.|
|[default](../../../parallel/openmp/reference/default-openmp.md)|병렬 영역 범위가 지정 되지 않은 변수 동작을 지정 합니다.|
|[firstprivate](../../../parallel/openmp/reference/firstprivate.md)|병렬 구문 전에 존재 하므로 각 스레드에 변수의 자체 인스턴스에 있어야 하 고 변수 값을 사용 하 여 변수를 초기화 해야 한다는 지정 합니다.|
|[if](../../../parallel/openmp/reference/if-openmp.md)|직렬 또는 병렬로 루프를 실행할지 여부를 지정 합니다.|
|[lastprivate](../../../parallel/openmp/reference/lastprivate.md)|변수는 바깥쪽 컨텍스트에서 버전 어떤 스레드가 실행 마지막 반복 (루프에 대 한 구성) 또는 마지막 섹션 (#pragma 섹션)의 개인 버전 설정 되어 있는지를 지정 합니다.|
|[nowait](../../../parallel/openmp/reference/nowait.md)|지시문에서 암시적 장애물을 재정의합니다.|
|[num_threads](../../../parallel/openmp/reference/num-threads.md)|스레드 팀에서 스레드 수를 설정합니다.|
|[ordered](../../../parallel/openmp/reference/ordered-openmp-clauses.md)|병렬에 필요한 [에 대 한](../../../parallel/openmp/reference/for-openmp.md) 문 경우는 [정렬](../../../parallel/openmp/reference/ordered-openmp-directives.md) 지시문은 루프에서 사용 됩니다.|
|[private](../../../parallel/openmp/reference/private-openmp.md)|각 스레드는 자체 인스턴스 변수를 지정 합니다.|
|[reduction](../../../parallel/openmp/reference/reduction.md)|각 스레드에 private는 하나 이상의 변수 끝의 병렬 영역 감소 작업의 제목을 지정 합니다.|
|[schedule](../../../parallel/openmp/reference/schedule.md)|에 적용 된 [에 대 한](../../../parallel/openmp/reference/for-openmp.md) 지시문입니다.|
|[shared](../../../parallel/openmp/reference/shared-openmp.md)|하나 이상의 변수는 모든 스레드 간에 공유 해야 지정 합니다.|

## <a name="see-also"></a>참고 항목

[OpenMP](../../../parallel/openmp/openmp-in-visual-cpp.md)<br/>
[지시문](../../../parallel/openmp/reference/openmp-directives.md)