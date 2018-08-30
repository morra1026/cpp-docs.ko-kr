---
title: 컴파일러 경고 (수준 1) C4953 | Microsoft Docs
ms.custom: ''
ms.date: 08/27/2018
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4953
dev_langs:
- C++
helpviewer_keywords:
- C4953
ms.assetid: 3c4f6ac6-3976-41ab-8a27-3c41d7472ea7
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 9e53808d4ad97bad4eccdf81b0a863277f8f7796
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43194634"
---
# <a name="compiler-warning-level-1-c4953"></a>컴파일러 경고(수준 1) C4953

> 인라인 '*함수*' 프로필 데이터가 수집 된 이후 편집 되었습니다.

사용 하는 경우 [/ltcg: pgupdate](../../build/reference/ltcg-link-time-code-generation.md), 컴파일러 후 컴파일된 입력된 모듈을 발견 `/LTCG:PGINSTRUMENT` 함수 (*함수*)는 편집 된 하 고 있고 기존 테스트 실행 식별 합니다 함수에 대 한 후보로 인라인 처리 합니다. 그러나 모듈을 다시 컴파일하면 함수가 더 이상 인라인 후보가 아닙니다.

이 경고는 정보 제공용입니다. 이 경고를 해결하려면 `/LTCG:PGINSTRUMENT`를 실행하고 모든 테스트 실행을 다시 수행한 다음 `/LTCG:PGOPTIMIZE`를 실행해야 합니다.

`/LTCG:PGOPTIMIZE` 를 사용한 경우 이 경고는 오류로 대체됩니다.