---
title: 컴파일러 오류 C3198 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3198
dev_langs:
- C++
helpviewer_keywords:
- C3198
ms.assetid: ec4ecf61-0067-4aa4-b443-a91013a1e59d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: bbb91d6f7b3ef6b8204a5f8bfb753db98ab6f93d
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46023386"
---
# <a name="compiler-error-c3198"></a>컴파일러 오류 C3198

부동 소수점 pragma 잘못 사용 했습니다: fenv_access pragma는 precise 모드 에서만에서 작동

[fenv_access](../../preprocessor/fenv-access.md) pragma에서 사용한를 [/fp](../../build/reference/fp-specify-floating-point-behavior.md) 이외의 다른 위치로 설정 **/fp: 정확한**합니다.

다음 샘플에서는 C3198 오류가 생성 됩니다.

```
// C3198.cpp
// compile with: /fp:fast
#pragma fenv_access(on)   // C3198
```