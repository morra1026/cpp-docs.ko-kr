---
title: . FPO | Microsoft Docs
ms.custom: ''
ms.date: 08/30/2018
ms.technology:
- cpp-masm
ms.topic: reference
f1_keywords:
- .FPO
dev_langs:
- C++
helpviewer_keywords:
- .FPO directive
ms.assetid: 35f4cd61-32f9-4262-b657-73f04f775d09
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: be5e20716ff414eea3eddc8490e2a3f82adeb777
ms.sourcegitcommit: a7046aac86f1c83faba1088c80698474e25fe7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43687747"
---
# <a name="fpo"></a>.FPO

합니다. FPO 지시문 디버그 레코드를.debug$ F 세그먼트 또는 섹션의 내보내기가 제어합니다.

## <a name="syntax"></a>구문

> FPO (*cdwLocals*를 *cdwParams*에 *cbProlog*를 *cbRegs*를 *fUseBP*,  *cbFrame*)

### <a name="parameters"></a>매개 변수

*cdwLocals*<br/>
지역 변수는 부호 없는 32 비트 값의 수입니다.

*cdwParams*<br/>
DWORD, 부호 없는 16 비트 값을 매개 변수 크기입니다.

*cbProlog*<br/>
함수 프롤로그 코드에서 부호 없는 8 비트 값을 바이트 수입니다.

*cbRegs*<br/>
저장 된 레지스터 번호입니다.

*fUseBP*<br/>
EBP 레지스터에 할당 되어 있는지 여부를 나타냅니다. 0 또는 1입니다.

*cbFrame*<br/>
프레임 유형을 나타냅니다.  참조 [FPO_DATA](/windows/desktop/api/winnt/ns-winnt-_fpo_data) 자세한 내용은 합니다.

## <a name="see-also"></a>참고자료

[지시문 참조](../../assembler/masm/directives-reference.md)<br/>