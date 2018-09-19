---
title: 컴파일러 경고 (수준 1) C4650 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4650
dev_langs:
- C++
helpviewer_keywords:
- C4650
ms.assetid: 3190b3e3-dcd6-4846-939b-f900ab652b2a
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d49b21452465f26d6e696f928c04c20dc0e33307
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46052898"
---
# <a name="compiler-warning-level-1-c4650"></a>컴파일러 경고(수준 1) C4650

미리 컴파일된 헤더에는 없는 정보가 디버깅 헤더의 전역 기호만 사용할 수 있습니다.

Microsoft 기호 디버깅 정보를 사용 하 여 미리 컴파일된 헤더 파일을 컴파일되지 않았습니다.

에 연결 하는 경우 결과 실행 파일 또는 동적 연결 라이브러리 파일의 미리 컴파일된 헤더에 포함 된 로컬 기호 디버깅 정보 포함 되지 않습니다.

이 경고를 사용 하 여 미리 컴파일된 헤더 파일을 컴파일하여 방지할 수 있습니다 합니다 [/Zi](../../build/reference/z7-zi-zi-debug-information-format.md) 명령줄 옵션입니다.