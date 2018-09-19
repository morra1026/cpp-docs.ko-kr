---
title: 인라인 어셈블리의 MASM 매크로 지시문 | Microsoft Docs
ms.custom: ''
ms.date: 08/30/2018
ms.technology:
- cpp-masm
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- directives, macros
- inline assembly, macro directives
- macros, directives
- MASM (Microsoft Macro Assembler), inline assembly macro directives
ms.assetid: 83643a09-1699-40a8-8ef2-13502bc4ac2c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 35ad22a9a4b79a31665ab6b156f8174d395bb0ee
ms.sourcegitcommit: fb9448eb96c6351a77df04af16ec5c0fb9457d9e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/13/2018
ms.locfileid: "43687975"
---
# <a name="masm-macro-directives-in-inline-assembly"></a>인라인 어셈블리의 MASM 매크로 지시문

**Microsoft 전용**

인라인 어셈블러는 매크로 어셈블러가 아닙니다. MASM 매크로 지시문을 사용할 수 없습니다 (**매크로**, `REPT`합니다 **IRC**를 `IRP`, 및 `ENDM`) 또는 매크로 연산자 (**<>**, **!** , **&** 하십시오 `%`, 및 `.TYPE`). 그러나 `__asm` 블록에 C 전처리기 지시문을 사용할 수 있습니다. 참조 [__asm 블록에서 c + + 또는 C를 사용 하 여](../../assembler/inline/using-c-or-cpp-in-asm-blocks.md) 자세한 내용은 합니다.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고자료

[__asm 블록에서 어셈블리 언어 사용](../../assembler/inline/using-assembly-language-in-asm-blocks.md)<br/>