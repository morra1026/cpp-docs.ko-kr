---
title: Intel&#39;MMX 명령 집합 s | Microsoft Docs
ms.custom: ''
ms.date: 08/30/2018
ms.technology:
- cpp-masm
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- MMX instruction set
ms.assetid: 705deb2d-c3fd-4696-9e22-8bcf25866daf
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 95f3cb57fc5c046057a5efa568ce930f13ca3256
ms.sourcegitcommit: a7046aac86f1c83faba1088c80698474e25fe7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43688355"
---
# <a name="intel39s-mmx-instruction-set"></a>Intel&#39;s MMX 명령 집합

**Microsoft 전용**

Visual C++ 컴파일러는 인라인 어셈블러에서 Intel의 MMX(멀티미디어 확장명) 명령 집합을 사용할 수 있도록 해 줍니다. 또한 MMX 명령은 디버거의 디스어셈블리에서 지원됩니다. 컴파일러는 함수에 MMX 명령이 포함되어 있지만 멀티미디어 상태를 비우는 EMMS 명령이 포함되어 있지 않은 경우 경고 메시지를 생성합니다. 자세한 내용은 Intel 웹 사이트를 참조하십시오.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고자료

[__asm 블록에서 어셈블리 언어 사용](../../assembler/inline/using-assembly-language-in-asm-blocks.md)<br/>