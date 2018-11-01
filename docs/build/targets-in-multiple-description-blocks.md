---
title: 여러 개의 설명 블록에 포함된 대상
ms.date: 11/04/2016
helpviewer_keywords:
- description blocks
- blocks, multiple description
- multiple description blocks
ms.assetid: 8618dcd9-c11d-4562-91a7-0c904ed438a8
ms.openlocfilehash: 5b441aab729beed771a6f3bce34e9555f490352d
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50647787"
---
# <a name="targets-in-multiple-description-blocks"></a>여러 개의 설명 블록에 포함된 대상

다른 명령을 사용 하 여 둘 이상의 설명 블록에 업데이트 하려면 대상 및 종속 항목 간의 연속 된 두 개의 콜론 (:)을 지정 합니다.

```
target.lib :: one.asm two.asm three.asm
    ml one.asm two.asm three.asm
    lib target one.obj two.obj three.obj
target.lib :: four.c five.c
    cl /c four.c five.c
    lib target four.obj five.obj
```

## <a name="see-also"></a>참고 항목

[대상](../build/targets.md)