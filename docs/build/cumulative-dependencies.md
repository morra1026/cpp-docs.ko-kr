---
title: 누적되는 종속 줄
ms.date: 11/04/2016
helpviewer_keywords:
- dependencies, cumulative
- cumulative dependencies in NMAKE
- dependencies
ms.assetid: fa6dd777-80b8-437d-87a7-aec0ed818a49
ms.openlocfilehash: c31740b830993c91568aea6d167fd3113b04fc57
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50460283"
---
# <a name="cumulative-dependencies"></a>누적되는 종속 줄

대상 반복 되 면 종속성 설명 블록에 누적 됩니다.

예를 들어이 규칙 집합에

```Output
bounce.exe : jump.obj
bounce.exe : up.obj
   echo Building bounce.exe...
```

이 평가 됩니다.

```Output
bounce.exe : jump.obj up.obj
   echo Building bounce.exe...
```

별도 설명 블록에 지정 된 각 하지만 마지막 종속성 줄에 있지 않은 대상 명령 블록을 사용 하지 않는 것 처럼 단일 설명 블록에 여러 종속성 줄에서 여러 대상으로 평가 됩니다. NMAKE 유추 규칙을 사용 하 여 이러한 대상에 대 한 하려고 합니다.

예를 들어이 규칙 집합에

```Output
leap.exe bounce.exe : jump.obj
bounce.exe climb.exe : up.obj
   echo Building bounce.exe...
```

이 평가 됩니다.

```Output

leap.exe : jump.obj
# invokes an inference rule
bounce.exe : jump.obj up.obj
   echo Building bounce.exe...
climb.exe : up.obj
   echo Building bounce.exe...
```

## <a name="see-also"></a>참고 항목

[대상](../build/targets.md)