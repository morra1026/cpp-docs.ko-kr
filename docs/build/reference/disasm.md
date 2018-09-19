---
title: /DISASM | Microsoft Docs
ms.date: 1/17/2018
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- /disasm
dev_langs:
- C++
helpviewer_keywords:
- -DISASM dumpbin option
- DISASM dumpbin option
- /DISASM dumpbin option
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 6a5a4d930c47d2a3c2808cbd0a343c5c68de4ac9
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45707189"
---
# <a name="disasm"></a>/DISASM

DUMPBIN 출력에 있는 코드 섹션의 디스어셈블리를 인쇄 합니다.

## <a name="syntax"></a>구문

> **/DISASM**{**:**\[**BYTES**|**NOBYTES**]}

### <a name="arguments"></a>인수

**BYTES**<br/>
디스어셈블리 출력에 해석 된 opcode 및 인수를 함께 명령 바이트를 포함합니다. 기본 옵션입니다.

**NOBYTES**<br/>
디스어셈블리 출력에는 명령 바이트는 포함 되지 않습니다.

## <a name="remarks"></a>설명

합니다 **/DISASM** 옵션 파일의 코드 섹션의 디스어셈블리를 표시 합니다. 디버그 기호를 사용 하 여 파일에 존재할 경우.

**/DISASM** 네이티브, 관리 되지 않는 이미지에만 사용 해야 합니다. 관리 코드에 해당 하는 도구는 [ILDASM](/dotnet/framework/tools/ildasm-exe-il-disassembler)합니다.

만 [/HEADERS](../../build/reference/headers.md) DUMPBIN 옵션에서 생성 된 파일에 사용할 수는 [/GL (전체 프로그램 최적화)](../../build/reference/gl-whole-program-optimization.md) 컴파일러 옵션입니다.

## <a name="see-also"></a>참고자료

[DUMPBIN 옵션](../../build/reference/dumpbin-options.md)
