---
title: NMAKE 심각한 오류 U1059 | Microsoft Docs
ms.custom: ''
ms.date: 08/27/2018
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- U1059
dev_langs:
- C++
helpviewer_keywords:
- U1059
ms.assetid: b21d9198-9c63-40d0-b589-80e17294ce24
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 8b54919398c757bfe05f747ff57341f31decfc61
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43200792"
---
# <a name="nmake-fatal-error-u1059"></a>NMAKE 심각한 오류 U1059

> 구문 오류: '}'에 종속 누락

종속 된 검색 경로 잘못 지정 되었습니다. 공백이 있거나 경로에 닫는 중괄호 (**}**)가 생략 되었습니다.

종속 된에 대 한 디렉터리 사양에 대 한 구문은

> **{** *디렉터리* **} 종속**

여기서 *디렉터리* 각 세미콜론으로 구분 된 하나 이상의 경로 지정 합니다 (**;**). 공백이 허용 됩니다.

매크로 의해 검색 경로의 전체 또는 일부를 대체 하면 공백 없이 매크로 확장에 있는지 확인 합니다.