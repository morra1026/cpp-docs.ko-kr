---
title: . PUSHFRAME | Microsoft Docs
ms.custom: ''
ms.date: 08/30/2018
ms.technology:
- cpp-masm
ms.topic: reference
f1_keywords:
- .PUSHFRAME
dev_langs:
- C++
helpviewer_keywords:
- .PUSHFRAME directive
ms.assetid: 17b123d0-4c6d-4fd2-85eb-798e8ad0a73c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c86ba043eb185e9cc5697f236b907ae8177d6824
ms.sourcegitcommit: a7046aac86f1c83faba1088c80698474e25fe7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43689491"
---
# <a name="pushframe"></a>.PUSHFRAME

생성 된 `UWOP_PUSH_MACHFRAME` 코드 항목을 해제 합니다. 경우 선택적 `code` 지정 된 경우 해제 코드 항목 1의 한정자를 지정 합니다. 그렇지 않은 경우 한정자는 0입니다.

## <a name="syntax"></a>구문

> . PUSHFRAME [코드]

## <a name="remarks"></a>설명

. PUSHFRAME ml64.exe 프레임 함수 해제 하는 방법을 지정할 수 있습니다 및에서 확장 하는 프롤로그 내 에서만 허용 됩니다 합니다 [PROC](../../assembler/masm/proc.md) 프레임 선언을 [합니다. 프롤로그 끝](../../assembler/masm/dot-endprolog.md) 지시문입니다. 이러한 지시문 코드를 생성 하지 않습니다. 만 생성할 `.xdata` 고 `.pdata`입니다. . 동작 스택이 없습니다을 실제로 구현 하는 지침 PUSHFRAME 보다 선행 되어야 합니다. 모두 해제 지시문 및 규약 확인 매크로에서 해제를 위한 코드를 래핑하는 것이 좋습니다.

자세한 내용은 [MASM (ml64.exe) x64](../../assembler/masm/masm-for-x64-ml64-exe.md)합니다.

## <a name="see-also"></a>참고자료

[지시문 참조](../../assembler/masm/directives-reference.md)<br/>