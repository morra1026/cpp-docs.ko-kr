---
title: 컴파일러 오류 C3083
ms.date: 11/04/2016
f1_keywords:
- C3083
helpviewer_keywords:
- C3083
ms.assetid: 05ff791d-52bb-41eb-9511-3ef89d7f4710
ms.openlocfilehash: 5ff049d3fcfb2c3dbc28baacdecee9b313574fc0
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50641407"
---
# <a name="compiler-error-c3083"></a>컴파일러 오류 C3083

'function': 왼쪽의 기호는 ': ' 형식 이어야 합니다

함수를 잘못 호출 했습니다.

## <a name="example"></a>예제

다음 샘플 C3083를 생성합니다.

```
// C3083.cpp
// compile with: /c
struct N {
   ~N();
};

struct N1 {
   ~N1();
};

N::N::~N() {}   // C3083
N1::~N1() {}   // OK
```