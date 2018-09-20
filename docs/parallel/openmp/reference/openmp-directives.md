---
title: OpenMP 지시문 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
dev_langs:
- C++
ms.assetid: 0562c263-344c-466d-843e-de830d918940
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 983a71920e9e7ce390ab8c64e81886db0d459450
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46389450"
---
# <a name="openmp-directives"></a>OpenMP 지시문

OpenMP API에서 사용 되는 지시문에 대 한 링크를 제공 합니다.

Visual c + +에서는 다음 OpenMP 지시문을 지원합니다.

|지시문|설명|
|---------------|-----------------|
|[atomic](../../../parallel/openmp/reference/atomic.md)|지정 하는 원자 단위로 업데이트 되는 메모리 위치입니다.|
|[barrier](../../../parallel/openmp/reference/barrier.md)|팀;의 모든 스레드를 동기화합니다. 모든 스레드가 장애물 모든 스레드가 장애물을 실행할 때까지 일시 중지 합니다.|
|[critical](../../../parallel/openmp/reference/critical.md)|한 번에 코드 한 스레드에서 실행만 되는지 지정 합니다.|
|[flush](../../../parallel/openmp/reference/flush-openmp.md)|모든 스레드 모든 공유 개체에 대 한 메모리의 동일한 보기를 지정 합니다.|
|[for](../../../parallel/openmp/reference/for-openmp.md)|하면에서 수행 된 작업을 여러 스레드로 분배 하는 병렬 영역 내부 루프에 대 한 합니다.|
|[master](../../../parallel/openmp/reference/master.md)|마스터 threadshould에만 실행할 프로그램의 섹션을 지정 합니다.|
|[ordered](../../../parallel/openmp/reference/ordered-openmp-directives.md)|해당 코드를 병렬에서 순차 루프와 같은 루프를 실행 해야 지정 합니다.|
|[parallel](../../../parallel/openmp/reference/parallel.md)|병렬로 여러 스레드에서 실행 될 코드는 병렬 영역을 정의 합니다.|
|[섹션](../../../parallel/openmp/reference/sections-openmp.md)|모든 스레드 간에 나눌 코드 섹션을 식별 합니다.|
|[single](../../../parallel/openmp/reference/single.md)|코드의 섹션 마스터 스레드 반드시 단일 스레드에서 실행할지를 지정할 수 있습니다.|
|[threadprivate](../../../parallel/openmp/reference/threadprivate.md)|변수는 스레드에 private 임을 지정 합니다.|

## <a name="see-also"></a>참고 항목

[OpenMP](../../../parallel/openmp/openmp-in-visual-cpp.md)<br/>
[절](../../../parallel/openmp/reference/openmp-clauses.md)