---
title: 컴파일러 오류 C2473 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2473
dev_langs:
- C++
helpviewer_keywords:
- C2473
ms.assetid: 6bb7dbf5-b198-490f-860e-fd64d0c2a284
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 0eeecedd3ad2cee551b6003912d9b7af32883588
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46026077"
---
# <a name="compiler-error-c2473"></a>컴파일러 오류 C2473

'identifier': 함수 정의로 보이지만 매개 변수 목록이 없습니다.

컴파일러가 매개 변수 목록 없이 함수처럼 보이는 항목을 발견했습니다.

## <a name="example"></a>예제

다음 샘플에서는 C2473을 생성합니다.

```
// C2473.cpp
// compile with: /clr /c
class A {
   int i {}   // C2473
};

class B {
   int i() {}   // OK
};
```