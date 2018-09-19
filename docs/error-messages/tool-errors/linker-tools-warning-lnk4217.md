---
title: 링커 도구 경고 LNK4217 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- LNK4217
dev_langs:
- C++
helpviewer_keywords:
- LNK4217
ms.assetid: 280dc03e-5933-4e8d-bb8c-891fbe788738
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 3c650eddd8078419f63df48cc91705d2e86eb5c8
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46067984"
---
# <a name="linker-tools-warning-lnk4217"></a>링커 도구 경고 LNK4217

'symbol' function '함수에서에서 가져온 기호를 로컬로 정의

[__declspec (dllimport)](../../cpp/dllexport-dllimport.md) 기호가 로컬로 정의 된 경우에 기호에 대해 지정 되었습니다. 제거 된 `__declspec` 이 경고를 해결 하려면 한정자입니다.

`symbol` 이미지 내에 정의 된 기호 이름이입니다. `function` 기호를 가져오는 함수가입니다.

옵션을 사용 하 여 컴파일하는 경우이 경고가 표시 되지 것입니다 [/clr](../../build/reference/clr-common-language-runtime-compilation.md)합니다.

LNK4217 대신 두 번째 모듈의 첫 번째 모듈 가져오기 라이브러리를 사용 하 여 컴파일해야 하는 경우 두 모듈을 함께 연결 하려는 경우에 발생할 수 있습니다.

```
// LNK4217.cpp
// compile with: /LD
#include "windows.h"
__declspec(dllexport) void func(unsigned short*) {}
```

그리고

```
// LNK4217b.cpp
// compile with: /c
#include "windows.h"
__declspec(dllexport) void func(unsigned short*) {}
```

이러한 두 모듈 연결 하려고 LNK4217 발생을 해결 하려면 첫 번째 샘플의 가져오기 라이브러리를 사용 하 여 두 번째 예제를 컴파일합니다.