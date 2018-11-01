---
title: 종속 줄의 부수적 효과
ms.date: 11/04/2016
helpviewer_keywords:
- dependencies, side effects
- NMAKE program, dependents
ms.assetid: d4e8db25-fdc0-4d73-81ec-1538f2e1b3e8
ms.openlocfilehash: 4ce32a55e89d78d45bc74ce3f7dd45ff2f99af31
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50530054"
---
# <a name="dependency-side-effects"></a>종속 줄의 부수적 효과

두 종속성 줄 다른 위치에 콜론 (:)를 사용 하 여 대상 지정 및 줄 중 하나에 다음 명령에 표시 하는 경우 인접 또는 조합 된 것 처럼 NMAKE 종속성을 해석 합니다. 에 명령이 나타나지 않지만 대신 종속성 하나의 설명 블록에 속해 있으며 다른 종속성을 사용 하 여 지정 된 명령을 실행 한다고 가정 하는 종속성에 대 한 유추 규칙을 호출 하지는 않습니다. 예를 들어이 규칙의 설정:

```Output
bounce.exe : jump.obj
   echo Building bounce.exe...

bounce.exe : up.obj
```

이 평가 됩니다.

```Output
bounce.exe : jump.obj up.obj
   echo Building bounce.exe...
```

이 적용 되지 않습니다 하는 경우 이중 콜론 (`::`) 사용 됩니다. 예를 들어이 규칙의 설정:

```Output
bounce.exe :: jump.obj
   echo Building bounce.exe...

bounce.exe :: up.obj
```

이 평가 됩니다.

```Output
bounce.exe : jump.obj
   echo Building bounce.exe...

bounce.exe : up.obj
# invokes an inference rule
```

## <a name="see-also"></a>참고 항목

[대상](../build/targets.md)