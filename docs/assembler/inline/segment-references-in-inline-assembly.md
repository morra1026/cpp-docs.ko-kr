---
title: 인라인 어셈블리의 참조 세그먼트 | Microsoft Docs
ms.custom: ''
ms.date: 08/30/2018
ms.technology:
- cpp-masm
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- references, inline assembly
- segment references in inline assembly
- inline assembly, segment references
- registers
- inline assembly, registers
- registers, inline assembly
ms.assetid: c63e6bb4-49d9-4fa1-bb22-eea21b5cbc0f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 792dda60407928aaf4a7d3fec2a61c0018b8b35a
ms.sourcegitcommit: a7046aac86f1c83faba1088c80698474e25fe7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43676391"
---
# <a name="segment-references-in-inline-assembly"></a>인라인 어셈블리의 세그먼트 참조

**Microsoft 전용**

이름 대신 레지스터로 세그먼트를 참조해야 합니다. 예를 들어 세그먼트 이름 `_TEXT`는 올바르지 않습니다. 세그먼트 재정의에서는 ES:[BX]와 같이 레지스터를 명시적으로 사용해야 합니다.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고자료

[__asm 블록에서 어셈블리 언어 사용](../../assembler/inline/using-assembly-language-in-asm-blocks.md)<br/>