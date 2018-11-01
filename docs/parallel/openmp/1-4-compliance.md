---
title: 1.4 규격
ms.date: 11/04/2016
ms.assetid: 662ad260-b9a1-43b7-b269-ef6ff0714e05
ms.openlocfilehash: 7fb47c9989e971e10701c2ee2bd7ac7823141812
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50642457"
---
# <a name="14-compliance"></a>1.4 규격

OpenMP C/c + + API의 구현은 *OpenMP 규격* 부록 3. 부록 A, B, D, E 및 F는 및 인식 하 고 화면에 보이는 대로 챕터 1, 2, 3, 4,이 사양의 모든 요소의 의미 체계를 유지 하는 경우 정보 목적 으로만 제공 되며 사양의 일부가 아닙니다. API의 하위 집합만 포함 하는 구현을 OpenMP 규격이 아닙니다.

OpenMP C 및 c + + API 구현에서 지원 되는 기본 언어 확장입니다. 기본 언어는이 문서의 언어 구문 이나 표시 되는 확장을 지원 하지 않으면, OpenMP 구현은 지원 하도록 않아도 됩니다.

모든 표준 C 및 c + + 라이브러리 함수 및 기본 제공 함수 (즉, 함수는 컴파일러에는 특정 기술 자료) 스레드로부터 안전 해야 합니다. 병렬 영역 내에서 서로 다른 스레드에 의해 스레드로부터 안전한 함수를 사용 하는 동기화 되지 않은 정의 되지 않은 동작을 생성 하지 않습니다. 그러나 동작을 동일 하 게 직렬 지역 수 없습니다 수 있습니다. (임의의 숫자 생성 함수에는 예입니다.)

OpenMP C/c + + API 지정 동작은 특정 *구현 시 정의 합니다.* 표준에 맞는 OpenMP 구현 정의 하 고 이러한 경우 해당 동작을 문서에 필요 합니다. 참조 [부록 E](../../parallel/openmp/e-implementation-defined-behaviors-in-openmp-c-cpp.md), 구현에서 정의 된 동작의 목록을 97 페이지입니다.