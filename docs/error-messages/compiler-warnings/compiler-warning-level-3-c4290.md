---
title: 컴파일러 경고 (수준 3) C4290 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4290
dev_langs:
- C++
helpviewer_keywords:
- C4290
ms.assetid: d1c6d85b-28e0-4a1f-9d48-23593337a6fb
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 3a6f09d8f3396381f34a0fbe3c7150b5948cee01
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46015975"
---
# <a name="compiler-warning-level-3-c4290"></a>컴파일러 경고(수준 3) C4290

C + + 예외 사양은 나타내는 함수를 제외 하 고 무시 됩니다. __declspec (nothrow) 아닙니다.

Visual c + + 허용 하지만 구현 되지 않는 예외 사양을 사용 하 여 함수를 선언 합니다. 다시 컴파일되지 않아도 컴파일 중에 무시 되는 지정 해야 하는 예외를 사용 하 여 코드와 연결 되도록 다시 나중에 예외 사양을 지 원하는 버전.

자세한 내용은 [예외 사양 (throw)](../../cpp/exception-specifications-throw-cpp.md) 합니다.

사용 하 여이 경고를 방지할 수 있습니다 합니다 [경고](../../preprocessor/warning.md) pragma:

```
#pragma warning( disable : 4290 )
```

다음 코드 샘플에서는 C4290 오류가 생성 됩니다.

```
// C4290.cpp
// compile with: /EHs /W3 /c
void f1(void) throw(int) {}   // C4290

// OK
void f2(void) throw() {}
void f3(void) throw(...) {}
```