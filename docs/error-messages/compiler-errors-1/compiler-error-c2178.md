---
title: 컴파일러 오류 C2178 | Microsoft Docs
ms.custom: ''
ms.date: 05/08/2017
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2178
dev_langs:
- C++
helpviewer_keywords:
- C2178
ms.assetid: 79a14158-17f3-4221-bd06-9d675c49cef4
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: af9efdb3258e6793a17a26b552df8ba4e63c9107
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46102341"
---
# <a name="compiler-error-c2178"></a>컴파일러 오류 C2178

'*식별자*'로 선언할 수 없습니다'*지정자*' 지정자

`mutable` 선언에서 지정자를 사용한 있지만 지정자를이 컨텍스트에서 허용 되지 않습니다.

합니다 `mutable` 지정자 클래스 데이터 멤버의 이름에만 적용 될 수 있으며 이름 선언에 적용할 수 없습니다 `const` 또는 `static`, 멤버를 참조 하는 적용할 수 없습니다.

## <a name="example"></a>예제

다음 샘플에서는 C2178 발생할 수 있습니다 하는 방법 및 해결 하는 방법을 보여 줍니다.

```
// C2178.cpp
// compile with: cl /c /W4 C2178.cpp

class S {
    mutable const int i; // C2178
    // To fix, declare either const or mutable, not both.
};

mutable int x = 4; // C2178
// To fix, remove mutable keyword
```
