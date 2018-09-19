---
title: FpCsr | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: dff95d5d-7589-4432-82db-64b459c24352
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a6ed0500d0382563878d0751ba5386e4cc637fdb
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45718291"
---
# <a name="fpcsr"></a>FpCsr

등록 상태에는 또한 x87 FPU 제어 단어입니다. 호출 규칙 nonvolatile 되도록이 레지스터를 지정 합니다.

프로그램 실행을 x87 FPU 제어 단어 레지스터의 시작 부분에 다음 표준 값으로 설정 됩니다.

```
FPCSR[0:6]: Exception masks all 1's (all exceptions masked)
FPCSR[7]: Reserved - 0
FPCSR[8:9]: Precision Control - 10B (double precision)
FPCSR[10:11]: Rounding  control - 0 (round to nearest)
FPCSR[12]: Infinity control - 0 (not used)
```

FPCSR 내의 필드를 수정 하는 호출 수신자는 호출자에 게 반환 하기 전에 해당를 복원 해야 합니다. 또한이 이러한 필드 중 하나를 수정 하는 호출자가 해당 문자열을 계약에 의해 호출 수신자는 수정 된 값이 필요 하지 않으면 호출 수신자를 호출 하기 전에 다른 표준 값으로 복원 해야 합니다.

제어 플래그의 비-변동성에 대 한 규칙의 두 가지 예외는

1. 비휘발성 FpCsr를 수정 하려면 지정 된 함수의 문서화 목적은 함수 플래그 지정 합니다.

1. 이 밖에도 경우 이러한 규칙 위반에는 이러한 규칙을 위반 하지 않은 예를 들어 전체 프로그램 분석을 통해 프로그램에서와 동일 하 게 동작/의미 하는 프로그램에서 결과 수정 합니다.

## <a name="see-also"></a>참고 항목

[호출 규칙](../build/calling-convention.md)