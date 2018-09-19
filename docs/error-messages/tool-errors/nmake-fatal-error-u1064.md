---
title: NMAKE 심각한 오류 U1064 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- U1064
dev_langs:
- C++
helpviewer_keywords:
- U1064
ms.assetid: 7141e66e-cde6-4173-84df-a391f3ebcdd1
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 4240bf2c553957e73d5ead0bdd03ea129450645b
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46093001"
---
# <a name="nmake-fatal-error-u1064"></a>NMAKE 심각한 오류 U1064

MAKEFILE을 찾을 수 및 지정 된 대상이 없습니다.

NMAKE 명령줄 메이크파일을 나 대상을 지정 하지 않았습니다 고 메이크파일 라는 파일을 현재 디렉터리에 없는 합니다.

NMAKE는 메이크파일 또는 명령줄 대상 (또는 둘 다)에 필요합니다. 메이크파일을 사용할 수 있도록 NMAKE를 /F 옵션을 지정 하거나 현재 디렉터리에서 메이크파일을 라는 파일을 배치 합니다. NMAKE는 메이크파일 제공 하지 않으면 유추 규칙을 사용 하 여 명령줄 대상을 만들 수 있습니다.