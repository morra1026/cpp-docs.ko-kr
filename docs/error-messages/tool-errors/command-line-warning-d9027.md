---
title: 명령줄 경고 D9027
ms.date: 11/04/2016
f1_keywords:
- D9027
helpviewer_keywords:
- D9027
ms.assetid: 2a29edc5-5649-48f2-9058-2057c747284c
ms.openlocfilehash: f89e7416efe7a0069ee2dae8df921933bbe76bcf
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50482604"
---
# <a name="command-line-warning-d9027"></a>명령줄 경고 D9027

소스 파일 '\<파일 이름 >' 무시

CL.exe 입력된 소스 파일을 무시 합니다.

/Fo 옵션 및 /c 옵션을 사용 하 여 명령줄에서 출력 파일 이름 사이 공백을 사용 하 여이 경고를 발생할 수 있습니다. 예를 들어:

```
cl /c /Fo output.obj input.c
```

/Fo 사이 공백이 있기 때문에 및 `output.obj`, CL.exe는 `output.obj` 입력된 파일의 이름으로 합니다. 이 문제를 해결 하려면 공간을 제거 합니다.

```
cl /c /Fooutput.obj input.c
```