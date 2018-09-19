---
title: 재귀 매크로 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- NMAKE program, recursion macros
- recursion macros
- macros, recursion
ms.assetid: c53e5ae7-619e-46b1-bdc2-86d8c7798b1d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f91a5f327686a522608b6eec9fd7106cbab00028
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45702042"
---
# <a name="recursion-macros"></a>재귀 매크로

재귀 매크로 사용 하 여 NMAKE를 재귀적으로 호출 합니다. 재귀 세션 Tools.ini 정보와 명령줄 및 환경 변수 매크로 상속 합니다. 메이크파일 정의한 유추 규칙을 상속 하지 않습니다 또는 **합니다. 접미사** 고 **입니다. 귀중 한** 사양입니다. 재귀 NMAKE 세션에는 매크로 전달 하려면 집합을 사용 하 여 재귀 호출 하기 전에 환경 변수를 설정, 재귀 호출에 대해 명령에서 매크로 정의 또는 Tools.ini에서 매크로 정의 합니다.

|매크로|정의|
|-----------|----------------|
|**확인**|원래 NMAKE를 호출 하는 데 사용 하는 명령입니다.<br /><br /> $(MAKE) 매크로 nmake.exe에 전체 경로 제공합니다.|
|**MAKEDIR**|NMAKE를 호출한 경우 현재 디렉터리입니다.|
|**MAKEFLAGS**|현재에서 옵션입니다. 사용 하 여 `/$(MAKEFLAGS)`입니다.  /F 포함 되지 않습니다.|

## <a name="see-also"></a>참고 항목

[특수 NMake 매크로](../build/special-nmake-macros.md)