---
title: NMAKE 심각한 오류 U1059
ms.date: 08/27/2018
f1_keywords:
- U1059
helpviewer_keywords:
- U1059
ms.assetid: b21d9198-9c63-40d0-b589-80e17294ce24
ms.openlocfilehash: 3c148bf2feb7ba12686e00b29f5bf90cb9f2f2d7
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50645027"
---
# <a name="nmake-fatal-error-u1059"></a>NMAKE 심각한 오류 U1059

> 구문 오류: '}'에 종속 누락

종속 된 검색 경로 잘못 지정 되었습니다. 공백이 있거나 경로에 닫는 중괄호 (**}**)가 생략 되었습니다.

종속 된에 대 한 디렉터리 사양에 대 한 구문은

> **{** *디렉터리* **} 종속**

여기서 *디렉터리* 각 세미콜론으로 구분 된 하나 이상의 경로 지정 합니다 (**;**). 공백이 허용 됩니다.

매크로 의해 검색 경로의 전체 또는 일부를 대체 하면 공백 없이 매크로 확장에 있는지 확인 합니다.