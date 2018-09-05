---
title: 어셈블리 언어 설명 | Microsoft Docs
ms.custom: ''
ms.date: 08/30/2018
ms.technology:
- cpp-masm
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- assembly language [C++], comments
- comments [C++], assembly language
- macros [C++], assembly language
- __asm keyword [C++], instructions
ms.assetid: 0dc10850-77f5-426e-9dab-185ea28e06e4
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 02f4c493bac5c2a066dc0b24e2a566d49345288d
ms.sourcegitcommit: a7046aac86f1c83faba1088c80698474e25fe7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43683328"
---
# <a name="assembly-language-comments"></a>어셈블리 언어 설명

**Microsoft 전용**

`__asm` 블록의 지침에서는 어셈블리 언어 주석을 사용할 수 있습니다.

```cpp
__asm mov ax, offset buff ; Load address of buff
```

C 매크로가 단일 논리 줄로 확장되기 때문에 매크로에서 어셈블리 언어 주석을 사용하지 마십시오. (참조 [C 매크로로 __asm 블록 정의](../../assembler/inline/defining-asm-blocks-as-c-macros.md).) `__asm` 블록 수도 C-스타일 주석도 포함할; 자세한 내용은 참조 하십시오 [__asm 블록에서 c + + 또는 C를 사용 하 여](../../assembler/inline/using-c-or-cpp-in-asm-blocks.md)입니다.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고자료

[__asm 블록에서 어셈블리 언어 사용](../../assembler/inline/using-assembly-language-in-asm-blocks.md)<br/>