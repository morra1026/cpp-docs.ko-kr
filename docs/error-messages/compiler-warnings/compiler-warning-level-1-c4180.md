---
title: 컴파일러 경고(수준 1) C4180
ms.date: 11/04/2016
f1_keywords:
- C4180
helpviewer_keywords:
- C4180
ms.assetid: 40c91bd4-37f1-4d59-a4f3-d5ddab68239b
ms.openlocfilehash: 8ed09edae5a9577773c573337b6e646a49599862
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50508868"
---
# <a name="compiler-warning-level-1-c4180"></a>컴파일러 경고(수준 1) C4180

함수 형식에 적용되는 한정자가 의미가 없으므로 무시됩니다.

**const**와 같은 한정자가 `typedef`로 정의된 함수 형식에 적용되었습니다.

## <a name="example"></a>예제

```
// C4180.cpp
// compile with: /W1 /c
typedef int FuncType(void);

// the const qualifier cannot be applied to the
// function type FuncType
const FuncType f;   // C4180
```