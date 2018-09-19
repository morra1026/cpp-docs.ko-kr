---
title: 여러 대상을 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- makefiles, targets
- multiple targets in NMAKE
- targets, multiple in NMAKE
- NMAKE program, targets
ms.assetid: b609a179-0b9f-4b08-9930-998047588ae0
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 66849bdbe28ac2bd965714de56f962df98ced133
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45703666"
---
# <a name="multiple-targets"></a>대상이 여러 개인 경우

NMAKE 별도 설명 블록에 지정 된 각 처럼 단일 종속성의 여러 대상 계산 합니다.

예를 들어,이 중...

```Output
bounce.exe leap.exe : jump.obj
   echo Building...
```

...이 계산 결과:

```Output
bounce.exe : jump.obj
   echo Building...
leap.exe : jump.obj
   echo Building...
```

## <a name="see-also"></a>참고 항목

[대상](../build/targets.md)