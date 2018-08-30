---
title: 컴파일러 경고 (수준 1) C4952 | Microsoft Docs
ms.custom: ''
ms.date: 08/27/2018
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4952
dev_langs:
- C++
helpviewer_keywords:
- C4952
ms.assetid: 593324f0-5cfe-42fb-b221-2f71308765dd
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f62f4c18380d89eb516a5fa49ef63e92ab79a6f2
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43207153"
---
# <a name="compiler-warning-level-1-c4952"></a>컴파일러 경고(수준 1) C4952

> '*함수*': 프로그램 데이터베이스에 프로필 데이터가 없습니다 '*pgd_file*'

사용 하는 경우 [/ltcg: pgupdate](../../build/reference/ltcg-link-time-code-generation.md), 컴파일러 후 컴파일된 입력된 모듈을 발견 `/LTCG:PGINSTRUMENT` 새 함수 (*함수*) 표시 합니다.

이 경고는 정보 제공용입니다. 이 경고를 해결하려면 `/LTCG:PGINSTRUMENT`를 실행하고 모든 테스트 실행을 다시 수행한 다음 `/LTCG:PGOPTIMIZE`를 실행해야 합니다.

`/LTCG:PGOPTIMIZE` 를 사용한 경우 이 경고는 오류로 대체됩니다.