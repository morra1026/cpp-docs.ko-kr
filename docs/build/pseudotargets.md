---
title: 의사 대상 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- makefiles, pseudotargets
- pseudotargets and NMAKE
- NMAKE program, pseudotargets
- timestamps, makefile pseudotargets
- NMAKE program, targets
ms.assetid: c8c479dc-0129-4186-8366-bc6251f2b494
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 56c0c0c93163759b604352a6e623f15726b8e7ec
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45715834"
---
# <a name="pseudotargets"></a>의사 대상

의사 대상은 종속 줄에서 파일 이름 대신 사용 되는 레이블입니다. 존재 하지 않는 이며 따라서 오래 된 파일으로 해석 됩니다. NMAKE 의사 대상의 타임 스탬프는 모든 종속 항목 중 가장 최근 가정 합니다. 없는 종속 된 경우 현재 가정 합니다. 의사를 대상으로 사용 하는 경우 해당 명령은 항상 실행 됩니다. 종속 된 것으로 사용 하는 의사 다른 종속성을 대상으로 야 합니다. 그러나 해당 종속성을 명령 블록을 가질 필요가 없습니다.

의사 대상 이름은 대상에 대 한 파일 이름 구문 규칙을 따릅니다. 그러나 이름에서 확장 되지 않은 경우 (즉, 포함 되지 않은 기간), 파일 이름에 대 한 8 자 제한을 초과할 수 있습니다 하 고 최대 256 자까지 사용할 수 있습니다.

## <a name="see-also"></a>참고 항목

[대상](../build/targets.md)