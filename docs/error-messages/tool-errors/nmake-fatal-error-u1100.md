---
title: NMAKE 심각한 오류 U1100
ms.date: 11/04/2016
f1_keywords:
- U1100
helpviewer_keywords:
- U1100
ms.assetid: c71910a7-c581-4d9c-a38c-d2d557d56289
ms.openlocfilehash: a1474acab4ca4929fb4db4b7b78d7a96637a0745
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50666598"
---
# <a name="nmake-fatal-error-u1100"></a>NMAKE 심각한 오류 U1100

매크로 '매크로 이름' 'rule' 일괄 처리 규칙의 컨텍스트에서 올바르지 않습니다.

NMAKE는 배치 모드 규칙의 명령 블록이 $<가 아닌 특수한 파일 매크로를 직접적 또는 간접적으로 참조할 때 이 오류를 생성합니다.

배치 모드 규칙에는 $< 매크로만 사용할 수 있습니다.