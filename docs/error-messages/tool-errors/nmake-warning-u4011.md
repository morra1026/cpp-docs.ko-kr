---
title: NMAKE 경고 U4011 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- U4011
dev_langs:
- C++
helpviewer_keywords:
- U4011
ms.assetid: e8244514-eba6-4285-8853-7baeefdcd8a4
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a1038ee86f76789451565ab6799795c851c95a95
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46118338"
---
# <a name="nmake-warning-u4011"></a>NMAKE 경고 U4011

'target': 사용할 수 있습니다; 모든 종속 항목 대상이 빌드되지 않았습니다.

지정된 된 대상의 종속성이 없어 또는 되었으며 및 종속 파일을 업데이트 하기 위한 명령이 0이 아닌 종료 코드를 반환 합니다. /K 옵션 NMAKE 빌드 관련 되지 않은 부분을 계속 처리 및 NMAKE 세션이 완료 되 면 종료 코드 1을 발급 하도록 지시 합니다.

이 경고는 경고 뒤 [U4010](../../error-messages/tool-errors/nmake-warning-u4010.md) 생성 또는 업데이트에 실패 한 각 종속에 대 한 합니다.