---
title: ML 심각 하지 않은 오류 A2050 | Microsoft Docs
ms.custom: ''
ms.date: 08/30/2018
ms.technology:
- cpp-masm
ms.topic: error-reference
f1_keywords:
- A2050
dev_langs:
- C++
helpviewer_keywords:
- A2050
ms.assetid: 16f3a58f-4bde-48f1-b0e3-2ed9612780a5
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: bd2e0e6c2fc818ef9286fd303c07a26bdd8b4e5a
ms.sourcegitcommit: a7046aac86f1c83faba1088c80698474e25fe7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43680673"
---
# <a name="ml-nonfatal-error-a2050"></a>ML 심각하지 않은 오류 A2050

**실시간 또는 BCD 수 없습니다**

부동 소수점 (실수) 또는 binary coded decimal (BCD) 상수를 사용한 이외의 데이터 이니셜라이저로 합니다.

다음 중 하나에 다음이 발생 했습니다.

- 실수 또는 BCD를 식에서 사용 되었습니다.

- 실수를 초기화 하는 데 지시문 이외의 [DWORD](../../assembler/masm/dword.md)를 [QWORD](../../assembler/masm/qword.md), 또는 [TBYTE](../../assembler/masm/tbyte.md)합니다.

- BCD를 초기화 하는 데 지시문 이외의 `TBYTE`합니다.

## <a name="see-also"></a>참고자료

[ML 오류 메시지](../../assembler/masm/ml-error-messages.md)<br/>