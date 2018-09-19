---
title: 컴파일러 경고 (수준 1) C4215 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4215
dev_langs:
- C++
helpviewer_keywords:
- C4215
ms.assetid: f2aab64d-1bab-4f75-95ee-89e1263047b1
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 137a278452e9e3e204d761f0519c16541cfdb46e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46094093"
---
# <a name="compiler-warning-level-1-c4215"></a>컴파일러 경고(수준 1) C4215

비표준 확장이 사용 됨: long float

기본 Microsoft 확장명 (/Ze) 취급 **float long** 으로 **double**합니다. ANSI 호환성 ([/Za](../../build/reference/za-ze-disable-language-extensions.md)) 하지 않습니다. 사용 하 여 **이중** 호환성을 유지 합니다.

다음 샘플에서는 C4215 오류가 생성 됩니다.

```
// C4215.cpp
// compile with: /W1 /LD
long float a;   // C4215

// use the line below to resolve the warning
// double a;
```