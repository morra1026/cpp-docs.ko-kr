---
title: Tools.ini 및 NMAKE | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- NMAKE program, reading files
- Tools.ini and NMake
ms.assetid: ebd5eab6-ddf4-430e-bf4a-1db5bb84e344
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 84406886c9aa0c0053ed7c183912bf8a7f1f4771
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45723582"
---
# <a name="toolsini-and-nmake"></a>Tools.ini와 NMAKE

NMAKE 읽습니다 Tools.ini 메이크파일에 읽기 전에 /R 사용 되지 않은 경우. 찾습니다 Tools.ini 먼저 현재 디렉터리에서 찾은 다음 INIT 환경 변수로 지정 된 디렉터리에서. NMAKE 설정 초기화 파일의 섹션으로 시작 `[NMAKE]` 한 메이크파일의 정보를 포함할 수 있습니다. 숫자 기호를 사용 하 여 시작 하는 별도 줄에 주석 지정 (#).

## <a name="see-also"></a>참고 항목

[NMAKE 실행](../build/running-nmake.md)