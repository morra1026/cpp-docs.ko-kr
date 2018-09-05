---
title: OPTION (MASM) | Microsoft Docs
ms.custom: ''
ms.date: 08/30/2018
ms.technology:
- cpp-masm
ms.topic: reference
f1_keywords:
- option
dev_langs:
- C++
helpviewer_keywords:
- OPTION directive
ms.assetid: 8e10dabd-e36f-4586-ab01-ada96736b0bd
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 09db749baf09525957faaf8af99434cc9775d0e7
ms.sourcegitcommit: a7046aac86f1c83faba1088c80698474e25fe7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43678047"
---
# <a name="option-masm"></a>OPTION (MASM)

있으며 어셈블러의 기능을 사용 하지 않도록 설정 합니다.

## <a name="syntax"></a>구문

> 옵션 *optionlist*

## <a name="remarks"></a>설명

사용 가능한 옵션은 다음과 같습니다.

|||||
|-|-|-|-|
|**CASEMAP**|**DOTNAME**|**NODOTNAME**|**에뮬레이터**|
|**NOEMULATOR**|**에필로그**|**EXPR16**|**EXPR32**|
|**언어**|**LJMP**|**NOLJMP**|**M510**|
|**NOM510**|**NOKEYWORD**|**NOSIGNEXTEND**|**OFFSET**|
|**OLDMACROS**|**NOOLDMACROS**|**OLDSTRUCTS**|**NOOLDSTRUCTS**|
|**PROC**|**프롤로그**|**읽기 전용**|**NOREADONLY**|
|**SCOPED**|**NOSCOPED**|**SEGMENT**|**SETIF2**합니다.|

언어에 대 한 구문은 **언어 옵션:**<em>x</em>여기서 *x* C, SYSCALL, STDCALL, PASCAL, FORTRAN, 또는 BASIC 중 하나입니다.  SYSCALL, PASCAL, FORTRAN, 및 BASIC은 지원 되지 않습니다 사용한 [합니다. 모델](../../assembler/masm/dot-model.md) 평면입니다.

## <a name="see-also"></a>참고자료

[지시문 참조](../../assembler/masm/directives-reference.md)<br/>