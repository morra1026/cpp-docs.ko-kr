---
title: ML 심각한 오류 A1007 | Microsoft Docs
ms.custom: ''
ms.date: 08/30/2018
ms.technology:
- cpp-masm
ms.topic: error-reference
f1_keywords:
- A1007
dev_langs:
- C++
helpviewer_keywords:
- A1007
ms.assetid: bcf9c826-beb3-4e93-91fe-1ffd34995fbf
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 539ab431510d5dc721e6531c11069a87e27c287a
ms.sourcegitcommit: a7046aac86f1c83faba1088c80698474e25fe7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43693603"
---
# <a name="ml-fatal-error-a1007"></a>ML 심각한 오류 A1007

**중첩 수준이 너무 많습니다.**

어셈블러에는 중첩 제한에 도달 합니다. 별도로 명시 20 수준으로 제한이 됩니다.

다음 중 하나를 너무 많이 중첩 되었습니다.

- 와 같은 높은 수준의 지시문 [합니다. IF](../../assembler/masm/dot-if.md), [합니다. 반복](../../assembler/masm/dot-repeat.md), 또는 [합니다. 하지만](../../assembler/masm/dot-while.md)합니다.

- 구조 정의입니다.

- 조건부 어셈블리 지시문입니다.

- 프로시저 정의 합니다.

- A [PUSHCONTEXT](../../assembler/masm/pushcontext.md) 지시문 (한도 10).

- 세그먼트 정의입니다.

- 포함 파일입니다.

- 매크로입니다.

## <a name="see-also"></a>참고자료

[ML 오류 메시지](../../assembler/masm/ml-error-messages.md)<br/>