---
title: 심각한 오류 C1853 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- devlang-cpp
ms.topic: error-reference
f1_keywords:
- C1853
dev_langs:
- C++
helpviewer_keywords:
- C1853
ms.assetid: ceb9b4a5-92bf-4573-8a9f-3109cc7743ce
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 016e5bbf064643ddff0f63c5e16a967ed914f3e2
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46044953"
---
# <a name="fatal-error-c1853"></a>심각한 오류 C1853

> '*filename*' 미리 컴파일된 헤더 파일이 이전 버전의 컴파일러에서 미리 컴파일된 헤더는 c + + 및 C에서 (또는 그 반대로) 사용 하는

가능한 원인:

- 미리 컴파일된 헤더는 이전 컴파일러 버전을 사용 하 여 컴파일 되었습니다. 다시 현재 컴파일러를 사용 하 여 헤더를 컴파일하십시오.

- 미리 컴파일된 헤더는 c + +에서 C 사용 하 여 사용에 대 한 헤더 중 하나를 지정 하 여 사용 하 고는 [/Tc](../../build/reference/tc-tp-tc-tp-specify-source-file-type.md) 컴파일러 옵션 또는 소스 파일의 접미사 "c"로 변경 합니다. 자세한 내용은 [미리 컴파일 코드에 대 한 두 가지 선택](../../build/reference/creating-precompiled-header-files.md#two-choices-for-precompiling-code)합니다.