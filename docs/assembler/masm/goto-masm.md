---
title: GOTO (MASM) | Microsoft Docs
ms.custom: ''
ms.date: 08/30/2018
ms.technology:
- cpp-masm
ms.topic: reference
f1_keywords:
- goto
dev_langs:
- C++
helpviewer_keywords:
- GOTO directive
ms.assetid: 6a5f73e7-6784-4eae-ac52-4fc77a7f369f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b0be678e2d39389cbc551c386c1890f799124b5b
ms.sourcegitcommit: a7046aac86f1c83faba1088c80698474e25fe7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43694002"
---
# <a name="goto-masm"></a>GOTO (MASM)

표시 된 줄에 어셈블리를 전송할 **:**_macrolabel_합니다.

## <a name="syntax"></a>구문

> **GOTO** *macrolabel*

## <a name="remarks"></a>설명

**GOTO** 안에서 허용 됩니다 [매크로](macro.md)를 [에 대 한](for-masm.md)를 [FORC](forc.md)를 [반복](repeat.md), 및 [하는동안](while-masm.md)블록입니다. 합니다 *macrolabel* 대상 줄에서 유일한 지시문 이어야 하며 선행 콜론 뒤에 야 합니다.

## <a name="see-also"></a>참고자료

[지시문 참조](../../assembler/masm/directives-reference.md)<br/>
