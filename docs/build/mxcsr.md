---
title: MxCsr
ms.date: 11/04/2016
ms.assetid: 4f3c229d-0862-4733-acc7-9ed7a0b870ce
ms.openlocfilehash: d411223634aec6d11413ac1f5b1fb04dba7498e1
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50497376"
---
# <a name="mxcsr"></a>MxCsr

등록 상태에 MxCsr도 포함 됩니다. Volatile 부분과 비휘발성 일부로이 레지스터를 분할 하는 호출 규칙입니다. Volatile 부분으로 이루어져 MXCSR 6 상태 플래그를 [0:5], [6:15] MXCSR 레지스터를 나머지 일시적이 아닌 것으로 간주 됩니다.

비휘발성 부분에는 프로그램 실행의 시작 부분에 다음과 같은 표준 값으로 설정 됩니다.

```
MXCSR[6]         : Denormals are zeros - 0
MXCSR[7:12]      : Exception masks all 1's (all exceptions masked)
MXCSR[13:14]   : Rounding  control - 0 (round to nearest)
MXCSR[15]      : Flush to zero for masked underflow - 0 (off)
```

MXCSR 내에서 비 volatile 필드를 수정 하는 호출 수신자는 호출자에 게 반환 하기 전에 해당를 복원 해야 합니다. 또한이 이러한 필드 중 하나를 수정 하는 호출자가 해당 문자열을 계약에 의해 호출 수신자는 수정 된 값이 필요 하지 않으면 호출 수신자를 호출 하기 전에 다른 표준 값으로 복원 해야 합니다.

제어 플래그의 비-변동성에 대 한 규칙의 두 가지 예외는

- 비휘발성 MxCsr를 수정 하려면 지정 된 함수의 문서화 목적은 함수 플래그 지정 합니다.

- 이 밖에도 경우 이러한 규칙 위반에는 이러한 규칙을 위반 하지 않은 예를 들어 전체 프로그램 분석을 통해 프로그램에서와 동일 하 게 동작/의미 하는 프로그램에서 결과 수정 합니다.

특히 함수의 설명서에 설명 된 경우가 아니면 함수 경계를 넘어 volatile 부분의 MXCSR 상태에 대 한 어떠한가 정도 하지를 만들 수 있습니다.

## <a name="see-also"></a>참고 항목

[호출 규칙](../build/calling-convention.md)