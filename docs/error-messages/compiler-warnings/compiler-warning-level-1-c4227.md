---
title: 컴파일러 경고 (수준 1) C4227 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4227
dev_langs:
- C++
helpviewer_keywords:
- C4227
ms.assetid: 78f98374-c00b-4000-aefa-1b1c67b4666b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: fda3a31b228f16b27f4bdefd3131a0ddcb90f5b5
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46060860"
---
# <a name="compiler-warning-level-1-c4227"></a>컴파일러 경고(수준 1) C4227

된 구문을 사용 했습니다: 참조의 한정자는 무시 됩니다.

와 같은 한정자를 사용 하 여 `const` 또는 `volatile` c + + 참조를 사용 하 여 쿼리로 됩니다.

## <a name="example"></a>예제

```
// C4227.cpp
// compile with: /W1 /c
int j = 0;
int &const i = j;   // C4227
```