---
title: EVEN 및 ALIGN 지시문 | Microsoft Docs
ms.custom: ''
ms.date: 08/30/2018
ms.technology:
- cpp-masm
ms.topic: conceptual
f1_keywords:
- align
- EVEN
dev_langs:
- C++
helpviewer_keywords:
- EVEN directive
- directives, MASM
- MASM (Microsoft Macro Assembler), directives
- NOP (no operation instruction)
- ALIGN directive
ms.assetid: 7357ab2d-4a5c-43ca-accb-a5f21cdfcde5
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 06a1007c50e3490e5b14e4da886494557be0d37e
ms.sourcegitcommit: a7046aac86f1c83faba1088c80698474e25fe7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43688303"
---
# <a name="even-and-align-directives"></a>EVEN 및 ALIGN 지시문

**Microsoft 전용**

인라인 어셈블러는 대부분의 MASM 지시문을 지원 하지 않을 수 있지만 지원지 않습니다 `EVEN` 하 고 **ALIGN**합니다. 이러한 지시문 배치 **NOP** (비 연산) 레이블을 특정 경계에 맞게 필요에 따라 어셈블리 코드에 대 한 지침입니다. 이를 통해 일부 프로세서에서 명령 페치 작업을 보다 효율적으로 수행할 수 있습니다.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고자료

[__asm 블록에서 어셈블리 언어 사용](../../assembler/inline/using-assembly-language-in-asm-blocks.md)<br/>