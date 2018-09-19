---
title: 매크로를 정의할 위치 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- defining macros
- macros, NMAKE
- NMAKE program, defining macros
ms.assetid: 0fc59ec5-5f58-4644-b7da-7b021f7001af
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 29a2899d7dba0b34c0ac3319c253c8056912d883
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45713819"
---
# <a name="where-to-define-macros"></a>매크로를 정의할 위치

명령줄, 명령 파일, 메이크파일 Tools.ini 파일에 매크로 정의 합니다.

메이크파일의 또는 Tools.ini 파일에서 각 매크로 정의 별도 줄에 표시 되 고 공백 또는 탭을 사용 하 여 시작할 수 없습니다. 공백이 나 탭 등호 앞뒤 무시 됩니다. 모든 [문자를 문자열](../build/defining-an-nmake-macro.md) 리터럴 주변 따옴표 및 공백이 포함 됩니다.

명령줄 또는 명령 파일에서 공백 및 탭 인수를 구분 하 고 등호를 묶을 수 없습니다. 경우 `string` 공백이 나 탭에 포함 된 큰따옴표를 문자열 자체 또는 매크로 전체를 묶습니다 ("").

## <a name="see-also"></a>참고 항목

[NMake 매크로 정의](../build/defining-an-nmake-macro.md)