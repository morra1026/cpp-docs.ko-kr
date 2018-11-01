---
title: .IF
ms.date: 08/30/2018
f1_keywords:
- .IF
helpviewer_keywords:
- .IF directive
ms.assetid: dccc7615-8fc7-4829-9f39-0ee405f6c1e3
ms.openlocfilehash: cf9c594d843c937dd2191bee2a7cebadbc615c82
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50483640"
---
# <a name="if"></a>.IF

테스트는 코드를 생성 `condition1` (예를 들어 AX > 7) 하 고 실행 합니다 *문을* 해당 조건이 true 인 경우.

## <a name="syntax"></a>구문

> . IF 조건 1<br/>
> 문<br/>
> [[. ELSEIF condition2<br/>
> 문]]<br/>
> [[. 다른<br/>
> 문]]<br/>
> .ENDIF

## <a name="remarks"></a>설명

경우는 [합니다. 다른](../../assembler/masm/dot-else.md) 원래 조건이 false 되었으면 같이 해당 문이 실행 됩니다. 조건을 런타임 시 계산 되는 참고 합니다.

## <a name="see-also"></a>참고자료

[지시문 참조](../../assembler/masm/directives-reference.md)<br/>