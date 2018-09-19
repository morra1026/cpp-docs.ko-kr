---
title: 종속 파일과 규칙을 유추 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- rules, inferred
- inferred dependents in NMAKE
- inferred rules in NMAKE
- dependents, inferred
ms.assetid: 9381e74a-53d9-445c-836d-0ff7ef6112d9
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c13ae7784ff40b39642ce26fd062a1aab80f2d4c
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45707553"
---
# <a name="inferred-dependents-and-rules"></a>유추된 종속 파일과 규칙

NMAKE 유추 해당 규칙이 있는 경우 대상에 대해 유추 된 종속을 가정 합니다. 규칙이 적용 되는 경우:

- *toext* 대상의 확장명과 일치 합니다.

- *fromext* 일치 하는 대상의 기본 이름 및 포함 된 파일의 확장명은 현재 또는 지정 된 디렉터리에 존재 합니다.

- *fromext* 중인 [합니다. 접미사](../build/dot-directives.md); 기타 *fromext* 일치 규칙에는 더 높은 **합니다. 접미사** 우선 순위입니다.

- 없는 명시적 종속 파일에 더 높은 **합니다. 접미사** 우선 순위입니다.

유추 된 종속 예기치 않은 부작용을 일으킬 수 있습니다. NMAKE의 대상의 설명 블록 명령이 포함 된 경우 규칙에 명령 대신 명령을 실행 합니다.

## <a name="see-also"></a>참고 항목

[유추 규칙](../build/inference-rules.md)