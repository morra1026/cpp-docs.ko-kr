---
title: 호출자-호출 수신자 저장 레지스터
ms.date: 11/04/2016
ms.assetid: 0533bd4b-d6bb-4ce1-8201-495e16870cbb
ms.openlocfilehash: f34fbfff8e6c61b5d568c073f6b7da2a12e34535
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50654703"
---
# <a name="callercallee-saved-registers"></a>호출자/호출 수신자 저장 레지스터

일시적인 것으로 간주 됩니다 및 고려해 야 RAX RCX, RDX, R8, R9에서 R10, R11 레지스터는 함수 호출에서 제거 (하지 않는 한 안전성이 전체 프로그램 최적화와 같은 분석을 통해).

레지스터 RBX, RBP, RDI, RSI, RSP, R12, R13, R14, 및 r 15 일시적이 아닌 것으로 간주 됩니다 저장 해야 및 함수에 의해 복원 하는 사용 합니다.

## <a name="see-also"></a>참고 항목

[호출 규칙](../build/calling-convention.md)