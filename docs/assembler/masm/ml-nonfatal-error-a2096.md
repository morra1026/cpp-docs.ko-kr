---
title: ML 심각 하지 않은 오류 A2096 | Microsoft Docs
ms.custom: ''
ms.date: 08/30/2018
ms.technology:
- cpp-masm
ms.topic: error-reference
f1_keywords:
- A2096
dev_langs:
- C++
helpviewer_keywords:
- A2096
ms.assetid: bab0b5ee-b39f-4e44-a41a-3f949fab4297
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 82f4ef76dca10b1208a931bc3e1cc09d82a639d2
ms.sourcegitcommit: a7046aac86f1c83faba1088c80698474e25fe7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43679600"
---
# <a name="ml-nonfatal-error-a2096"></a>ML 심각하지 않은 오류 A2096

**세그먼트, 그룹 또는 세그먼트 레지스터가 필요 합니다.**

세그먼트 또는 그룹에 필요 하지만 찾을 수 없습니다.

다음 중 하나에 다음이 발생 했습니다.

- 연산자를 재정의 하는 세그먼트를 사용 하 여 지정 된 왼쪽된 피연산자 (**:**) 세그먼트 레지스터 (CS, DS, SS, ES, FS 또는 GS) 그룹 이름, 세그먼트 이름 또는 세그먼트 식이 없습니다.

- 합니다 [가정](../../assembler/masm/assume.md) 지시문에는 유효한 세그먼트 주소, 세그먼트 등록, 그룹 또는 특수 한 없이 세그먼트 레지스터를 지정 된 **플랫** 그룹입니다.

## <a name="see-also"></a>참고자료

[ML 오류 메시지](../../assembler/masm/ml-error-messages.md)<br/>