---
title: NMAKE 심각한 오류 U1099
ms.date: 11/04/2016
f1_keywords:
- U1099
helpviewer_keywords:
- U1099
ms.assetid: 6688a805-43e6-4247-a2d0-14be082f0b13
ms.openlocfilehash: 395f25d8d27bc5e9b6132c87390c8c3bc19b6cc4
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50631220"
---
# <a name="nmake-fatal-error-u1099"></a>NMAKE 심각한 오류 U1099

스택 오버플로

처리 중인 메이크파일 현재 스택 할당 NMAKE에 대해 너무 복잡 했습니다. NMAKE (12 K) 0x3000 할당을 있습니다.

NMAKE의 스택 할당을 늘리려면 다음을 실행 합니다 [/stack editbin](../../build/reference/stack.md) 큰 스택 옵션을 사용 하 여 유틸리티.

**NMAKE /STACK:reserve editbin 합니다. EXE**

여기서 *예약할* 숫자로 NMAKE에서 현재 스택 할당 보다 큽니다.