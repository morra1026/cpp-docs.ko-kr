---
title: 4. 환경 변수 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 4ec7ed81-e9ca-46a1-84f8-8f9ce4587346
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: aec56dad334dcd27de2068e660ff8ec5a6e72f90
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46415497"
---
# <a name="4-environment-variables"></a>4. 환경 변수

OpenMP C 및 c + + API 환경 변수 (또는 해당 하는 플랫폼별 메커니즘)이이 장에서 설명 하는 병렬 코드의 실행을 제어 합니다.  환경 변수 이름이 대문자 여야 합니다. 에 할당 된 값은 대/소문자 구분 되며 선행 및 후행 공백은 있을 수 있습니다.  수정 프로그램을 시작한 후 값은 무시 됩니다.

환경 변수는 다음과 같습니다.

- **OMP_SCHEDULE** 런타임 일정 유형 및 청크 크기를 설정 합니다.

- **OMP_NUM_THREADS** 실행 하는 동안 사용할 스레드 수를 설정 합니다.

- **OMP_DYNAMIC** 설정 하거나 해제 스레드 수를 동적으로 조정 합니다.

- **OMP_NESTED** 하거나 중첩 된 병렬 처리를 사용 하지 않도록 설정 합니다.

이 챕터에 예제만 Unix C 셸 (csh) 환경에서 이러한 변수를 설정할 수 있습니다 하는 방법을 보여 줍니다. Korn에서 셸 및 DOS 환경 작업은 마찬가지로 다음과 같습니다.

csh: setenv OMP_SCHEDULE "dynamic"

ksh: OMP_SCHEDULE 내보내기 "동적" =

: DOS OMP_SCHEDULE 설정 = "동적"