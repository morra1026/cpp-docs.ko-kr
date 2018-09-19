---
title: 심각한 오류 C1307 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C1307
dev_langs:
- C++
helpviewer_keywords:
- C1307
ms.assetid: 6f77d3d4-ba8a-476c-b540-aff19eb4efc4
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 65f398dd9885c571ea0d66171889f20d3321a3b9
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46085864"
---
# <a name="fatal-error-c1307"></a>심각한 오류 C1307

프로필 데이터가 수집된 이후 프로그램이 편집되었습니다.

사용 하는 경우 [/ltcg: pgoptimize](../../build/reference/ltcg-link-time-code-generation.md), 링커 /ltcg: pginstrument 후 컴파일된 입력된 모듈을 검색 및 모듈에 없는 기존 프로필 데이터는 더 이상 관련이 지점에 변경 된 것입니다. 예를 들어 호출 그래프 다시 컴파일된 모듈에서 변경 된 경우 컴파일러에서 C1307를 생성 합니다.

이 오류를 해결 하려면 /ltcg: pginstrument 실행, 모든 테스트 실행을 다시 실행 하 고 /ltcg: pgoptimize를 실행 합니다. 실행 /ltcg: pginstrument 및 다시 실행 된 모든 테스트를 실행할 수 없습니다, 경우에 최적화 된 이미지를 만드는 /ltcg: pgupdate /ltcg: pgoptimize 대신 사용 합니다.