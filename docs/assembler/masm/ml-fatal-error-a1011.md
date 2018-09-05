---
title: ML 심각한 오류 A1011 | Microsoft Docs
ms.custom: ''
ms.date: 08/30/2018
ms.technology:
- cpp-masm
ms.topic: error-reference
f1_keywords:
- A1011
dev_langs:
- C++
helpviewer_keywords:
- A1011
ms.assetid: 7fbf092d-4189-4330-a884-dfa2268fc3dd
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 32949773b869d189516a381ca7df941760a1e4e4
ms.sourcegitcommit: a7046aac86f1c83faba1088c80698474e25fe7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43690810"
---
# <a name="ml-fatal-error-a1011"></a>ML 심각한 오류 A1011

**지시문은 제어 블록에에 있어야 합니다.**

어셈블러 찾을 상위 수준 지시문 여기서 하나를 사용할 수 없습니다. 다음 지시문 중 하나를 찾을 수 있습니다.

- [. ELSE](../../assembler/masm/dot-else.md) 없이 [합니다. 경우에](../../assembler/masm/dot-if.md)

- [. ENDIF](../../assembler/masm/dot-endif.md) 없이 [합니다. 경우에](../../assembler/masm/dot-if.md)

- [. ENDW](../../assembler/masm/dot-endw.md) 없이 [합니다. WHILE](../../assembler/masm/dot-while.md)

- [. UNTILCXZ](../../assembler/masm/dot-untilcxz.md) 없이 [합니다. 반복](../../assembler/masm/dot-repeat.md)

- [. 계속 진행](../../assembler/masm/dot-continue.md) 없이 [합니다. 하는 동안](../../assembler/masm/dot-while.md) 또는 [합니다. 반복](../../assembler/masm/dot-repeat.md)

- [. 중단](../../assembler/masm/dot-break.md) 없이 [합니다. 하는 동안](../../assembler/masm/dot-while.md) 또는 [합니다. 반복](../../assembler/masm/dot-repeat.md)

- [. 다른](../../assembler/masm/dot-else.md) 다음 `.ELSE`

## <a name="see-also"></a>참고자료

[ML 오류 메시지](../../assembler/masm/ml-error-messages.md)<br/>