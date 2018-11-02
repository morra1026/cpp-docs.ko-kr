---
title: 대상이 여러 개인 경우
ms.date: 11/04/2016
helpviewer_keywords:
- makefiles, targets
- multiple targets in NMAKE
- targets, multiple in NMAKE
- NMAKE program, targets
ms.assetid: b609a179-0b9f-4b08-9930-998047588ae0
ms.openlocfilehash: 2762e458781e3a95f478ea3477fc8ef02f9196fb
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50645063"
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