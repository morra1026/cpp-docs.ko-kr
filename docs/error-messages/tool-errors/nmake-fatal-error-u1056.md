---
title: NMAKE 심각한 오류 U1056 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- U1056
dev_langs:
- C++
helpviewer_keywords:
- U1056
ms.assetid: da855728-b69e-413c-83ed-df912126215e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: e0a83c62bedf995708d5e99fee19f05696d05c2d
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46065701"
---
# <a name="nmake-fatal-error-u1056"></a>NMAKE 심각한 오류 U1056

명령 처리기를 찾을 수 없습니다.

명령 프로세서에 지정 된 경로에 없습니다. 합니다 **COMSPEC** 하거나 **경로** 환경 변수입니다.

NMAKE는 COMMAND.COM 또는 cmd.를 사용합니다. Exe 명령을 실행할 때 명령 프로세서로 사용 합니다. 에 설정 된 경로에 명령 프로세서를 먼저 찾고 **COMSPEC**합니다. 하는 경우 **COMSPEC** NMAKE 검색에 지정 된 디렉터리가 존재 하지 않는 **경로**합니다.