---
title: 컴파일러 경고(수준 1) C4227
ms.date: 11/04/2016
f1_keywords:
- C4227
helpviewer_keywords:
- C4227
ms.assetid: 78f98374-c00b-4000-aefa-1b1c67b4666b
ms.openlocfilehash: a93b7f225149f9b557ad6238376ffd1bafec82d3
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50550308"
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