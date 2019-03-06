---
title: 대상이 여러 개인 경우
ms.date: 11/04/2016
helpviewer_keywords:
- makefiles, targets
- multiple targets in NMAKE
- targets, multiple in NMAKE
- NMAKE program, targets
ms.assetid: b609a179-0b9f-4b08-9930-998047588ae0
ms.openlocfilehash: 28ac69a6e724b4e7c6fe838e0de3703cbdf0cfaa
ms.sourcegitcommit: bff17488ac5538b8eaac57156a4d6f06b37d6b7f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57421431"
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

## <a name="see-also"></a>참고자료

[대상](../build/targets.md)
