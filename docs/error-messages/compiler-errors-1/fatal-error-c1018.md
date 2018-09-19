---
title: 심각한 오류 C1018 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C1018
dev_langs:
- C++
helpviewer_keywords:
- C1018
ms.assetid: 2ceb8a99-30b2-4b80-bf42-e9f3305b3c52
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 5549cdd40b8287f75f80b0e633ff053a23cdecde
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46034449"
---
# <a name="fatal-error-c1018"></a>심각한 오류 C1018

예기치 않은 #elif입니다.

`#elif` 지시문이 `#if`, `#ifdef`또는 `#ifndef` 구문 외부에 표시됩니다. `#elif` 는 이러한 구문 중 하나 내에서만 사용합니다.

다음 샘플에서는 C1018을 생성합니다.

```
// C1018.cpp
#elif      // C1018
#endif

int main() {}
```

해결 방법:

```
// C1018b.cpp
#if 1
#elif
#endif

int main() {}
```