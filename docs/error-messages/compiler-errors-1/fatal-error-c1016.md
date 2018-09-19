---
title: 심각한 오류 C1016 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C1016
dev_langs:
- C++
helpviewer_keywords:
- C1016
ms.assetid: 33f45c3e-2d8f-43ad-a445-c412d1d54ce1
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 72da7f9413724fe83352e888eff8b5e577fb0eda
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46052259"
---
# <a name="fatal-error-c1016"></a>심각한 오류 C1016

\#ifdef 예상 #ifndef에는 식별자는 식별자가 필요 합니다.

조건부 컴파일 지시문([#ifdef](../../preprocessor/hash-ifdef-and-hash-ifndef-directives-c-cpp.md) 또는 `#ifndef`)에 평가할 식별자가 없습니다. 오류를 해결하려면 식별자를 지정합니다.

다음 샘플에서는 C1016을 생성합니다.

```
// C1016.cpp
#ifdef   // C1016
#define FC1016
#endif

int main() {}
```

해결 방법:

```
// C1016b.cpp
#ifdef X
#define FC1016
#endif

int main() {}
```