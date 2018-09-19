---
title: 컴파일러 경고 (수준 1) C4006 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4006
dev_langs:
- C++
helpviewer_keywords:
- C4006
ms.assetid: f1a59819-0fd2-4361-8e3a-99e4b514b8e1
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 35987244498b95dfee6f285f100237c3d3a361ea
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46037049"
---
# <a name="compiler-warning-level-1-c4006"></a>컴파일러 경고(수준 1) C4006

\#undef에 식별자가 필요

`#undef` 지시문에서 정의 해제할 식별자를 지정하지 않았습니다. 지시문이 무시됩니다. 이 경고를 해결하려면 식별자를 지정해야 합니다. 다음 샘플에서는 C4006을 생성합니다.

```
// C4006.cpp
// compile with: /W1
#undef   // C4006

// try..
// #undef TEST

int main() {
}
```