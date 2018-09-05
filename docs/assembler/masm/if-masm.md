---
title: IF (MASM) | Microsoft Docs
ms.custom: ''
ms.date: 08/30/2018
ms.technology:
- cpp-masm
ms.topic: reference
f1_keywords:
- if
dev_langs:
- C++
helpviewer_keywords:
- IF directive
ms.assetid: 82e43712-4f0c-4bf6-90ce-0663e81af707
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ca0cce834924f7fc147b1ef301d5bd345dfd2973
ms.sourcegitcommit: a7046aac86f1c83faba1088c80698474e25fe7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43685309"
---
# <a name="if-masm"></a>IF (MASM)

어셈블리의 부여 *ifstatements* 하는 경우 *expression1* 가 true (0이 아닌) 또는 *elseifstatements* 경우 *expression1* 이 false (0) 및 *expression2* 그렇습니다.

## <a name="syntax"></a>구문

> IF *expression1*<br/>
> *ifstatements*<br/>
> [[ELSEIF *expression2*<br/>
> *elseifstatements*]]<br/>
> [[다른<br/>
> *elsestatements*]]<br/>
> ENDIF

## <a name="remarks"></a>설명

다음 지시문 대신 사용할 수 있습니다 [ELSEIF](../../assembler/masm/elseif-masm.md): **ELSEIFB**, **ELSEIFDEF**하십시오 **ELSEIFDIF**, **ELSEIFDIFI** , **ELSEIFE**를 **ELSEIFIDN**를 **ELSEIFIDNI**를 **ELSEIFNB**, 및 **ELSEIFNDEF** . 필요에 따라 조합 *elsestatements* 이전 식이 false 인 경우. 어셈블리 타임 식 계산 되는 참고 합니다.

## <a name="see-also"></a>참고자료

[지시문 참조](../../assembler/masm/directives-reference.md)<br/>