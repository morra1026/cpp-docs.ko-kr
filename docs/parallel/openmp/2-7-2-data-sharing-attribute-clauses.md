---
title: 2.7.2 데이터 공유 특성 절
ms.date: 11/04/2016
ms.assetid: 47347d3c-18bd-441f-99cf-7737564c417f
ms.openlocfilehash: 4c9209a4d627c6212087b621b223a3fb81b48ce3
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50559655"
---
# <a name="272-data-sharing-attribute-clauses"></a>2.7.2 데이터 공유 특성 절

여러 지시문 영역의 기간에 대 한 변수 공유 특성을 제어 하는 사용자를 허용 하는 절을 적용 합니다. 공유 특성 절 절은 표시 되는 지시문의 어휘 범위에서 변수에 적용 됩니다. 다음 절 중 일부만 모든 지시문에 허용 됩니다. 지시문을 사용 하 여 특정 지시문에서 사용할 수 있는 절 목록 설명 되어 있습니다.

변수가 표시 하면 병렬 작업 공유 생성자가 발견 되 면 공유 특성 절에 변수를 지정 하지 않으면 경우 또는 **threadprivate** 지시문에 다음 변수 공유 됩니다. 병렬 영역 동적 범위 내에 선언 된 정적 변수 공유 됩니다. 힙 메모리를 할당 (예를 들어,를 사용 하 여 **malloc ()** C 또는 c + + 또는 **새** c + +에서 연산자)를 공유 합니다. 그러나이 메모리에 대 한 포인터 일 수 있습니다 전용 또는 공유 합니다. 병렬 영역 동적 범위 내에 선언 된 자동 저장 기간이 있는 변수는 private입니다.

절의 대부분 동의 *변수 목록* 쉼표로 구분 된 목록이 표시 되는 변수는 인수입니다. 변수가 참조 하는 경우 데이터 공유 특성 절에 템플릿에서 파생 된 형식 및 다른 프로그램에서 해당 변수 참조가, 동작이 정의 되지 않습니다.

지시문 절 내에 나타나는 모든 변수 표시 되어야 합니다. 필요에 따라 절을 반복 될 수 있습니다 하지만 변수가 없기 변수 둘 다 지정할 수 있습니다 한다는 점을 제외 하면 둘 이상의 절에 지정할 수 있습니다는 **firstprivate** 와 **lastprivate** 절.

다음 섹션에서는 데이터 공유 특성 절을 설명합니다.

- **개인**하십시오 [2.7.2.1 섹션](../../parallel/openmp/2-7-2-1-private.md) 25 페이지입니다.

- **firstprivate**하십시오 [2.7.2.2 섹션](../../parallel/openmp/2-7-2-2-firstprivate.md) 26 페이지입니다.

- **lastprivate**하십시오 [2.7.2.3 섹션](../../parallel/openmp/2-7-2-3-lastprivate.md) 27 페이지입니다.

- **공유**하십시오 [2.7.2.4 섹션](../../parallel/openmp/2-7-2-4-shared.md) 27 페이지입니다.

- **기본**하십시오 [2.7.2.5 섹션](../../parallel/openmp/2-7-2-5-default.md) 28 페이지입니다.

- **감소**하십시오 [2.7.2.6 섹션](../../parallel/openmp/2-7-2-6-reduction.md) 28 페이지입니다.

- **copyin**하십시오 [2.7.2.7 섹션](../../parallel/openmp/2-7-2-7-copyin.md) 31 페이지입니다.

- **copyprivate**하십시오 [2.7.2.8 섹션](../../parallel/openmp/2-7-2-8-copyprivate.md) 32 페이지입니다.