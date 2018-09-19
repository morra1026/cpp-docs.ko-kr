---
title: 컴파일러 오류 C2710 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2710
dev_langs:
- C++
helpviewer_keywords:
- C2710
ms.assetid: a2a6bb5b-86ad-4a6c-acd0-e2bef8464e0e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 94b95ce0a87a2ba894dde2ba41c0e7d704c477b6
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46112800"
---
# <a name="compiler-error-c2710"></a>컴파일러 오류 C2710

'construct': '__declspec(modifier)'에 대 한 포인터를 반환 하는 함수에만 적용 될 수 있습니다

반환 값이 함수는 유일한 구문입니다 `modifier` 적용할 수 있습니다.

다음 샘플에서는 C2710 오류가 생성 됩니다.

```
// C2710.cpp
__declspec(restrict) void f();   // C2710
// try the following line instead
__declspec(restrict) int * g();
```