---
title: EXTERNDEF | Microsoft Docs
ms.custom: ''
ms.date: 08/30/2018
ms.technology:
- cpp-masm
ms.topic: reference
f1_keywords:
- EXTERNDEF
dev_langs:
- C++
helpviewer_keywords:
- EXTERNDEF directive
ms.assetid: 95a10de6-c345-4428-a2f2-90f7d411dc86
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d5c3d42cabb88c38ce1d98da24cd2cb4ddec8d5b
ms.sourcegitcommit: a7046aac86f1c83faba1088c80698474e25fe7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43683663"
---
# <a name="externdef"></a>EXTERNDEF

하나 이상의 외부 변수, 레이블 또는 이라는 기호를 정의 *이름을* 형식인 `type`합니다.

## <a name="syntax"></a>구문

> EXTERNDEF [[langtype]] 이름: 유형 [[, [[langtype]] 이름: type]]...

## <a name="remarks"></a>설명

하는 경우 *이름을* 정의 된 모듈의 것으로 간주 됩니다 [공용](../../assembler/masm/public-masm.md)합니다. 하는 경우 *이름을* 참조 하는 모듈의 것으로 간주 됩니다 [EXTERN](../../assembler/masm/extern-masm.md)합니다. 하는 경우 *이름을* 가 참조 되지 않으면이 무시 합니다. 합니다 `type` 될 수 있습니다 [ABS](../../assembler/masm/operator-abs.md), 가져오는 *이름* 상수입니다. 일반적으로 사용 되는 파일 포함 합니다.

## <a name="see-also"></a>참고자료

[지시문 참조](../../assembler/masm/directives-reference.md)<br/>