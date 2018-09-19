---
title: 유추 된 종속 파일 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- inferred dependents in NMAKE
- dependents, inferred
ms.assetid: 9303045c-69b3-4f35-bffc-19d5cd6ea3c3
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 631c5631b60f0e05dd1f1541facc767f35944d3d
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45701482"
---
# <a name="inferred-dependents"></a>유추된 종속 파일

유추 된 종속 유추 규칙에서 파생 되 고 명시적 종속 항목 보다 먼저 계산 됩니다. 유추 된 종속 대상 관련 하 여 오래 된 경우 NMAKE 종속성에 대 한 명령 블록을 호출 합니다. 유추 된 종속 파일이 존재 하지 않거나 자체 종속 항목에 대해 오래 된, 경우 NMAKE는 먼저 유추 된 종속 파일을 업데이트 합니다. 유추 된 종속 항목에 대 한 자세한 내용은 참조 하세요. [유추 규칙](../build/inference-rules.md)합니다.

## <a name="see-also"></a>참고 항목

[종속 파일](../build/dependents.md)