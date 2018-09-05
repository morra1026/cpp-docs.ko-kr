---
title: 호출 | Microsoft Docs
ms.custom: ''
ms.date: 08/30/2018
ms.technology:
- cpp-masm
ms.topic: reference
f1_keywords:
- Invoke
dev_langs:
- C++
helpviewer_keywords:
- INVOKE directive
ms.assetid: 12d9bb40-33b9-411e-b801-45a1d675967e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 3e5698acf9986903a1d6d731c1047484a0ce6904
ms.sourcegitcommit: a7046aac86f1c83faba1088c80698474e25fe7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43676519"
---
# <a name="invoke"></a>INVOKE

제공한 주소로 프로시저 호출 *식*, 언어 형식의 표준 호출 규칙에 따라 레지스터 나 스택에 인수를 전달 합니다.

## <a name="syntax"></a>구문

> INVOKE *식을* [[합니다 *인수*]]

## <a name="remarks"></a>설명

프로시저에 전달 되는 각 인수 식을, 레지스터 쌍으로, 또는 주소 식일 수 있습니다 (앞에 식을 `ADDR`).

## <a name="see-also"></a>참고자료

[지시문 참조](../../assembler/masm/directives-reference.md)<br/>