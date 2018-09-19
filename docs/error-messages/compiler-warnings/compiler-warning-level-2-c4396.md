---
title: 컴파일러 경고 (수준 2) C4396 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4396
dev_langs:
- C++
helpviewer_keywords:
- C4396
ms.assetid: 7cd6b283-db17-4574-b299-03e0b913ad70
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: fa0a084e90db9d48f517bfe65c6340eb532f0ae6
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46118572"
---
# <a name="compiler-warning-level-2-c4396"></a>컴파일러 경고(수준 2) C4396

"name": friend 선언이 함수 템플릿의 특수화를 참조하는 경우 인라인 지정자를 사용할 수 없습니다.

함수 템플릿의 특수화 중 하나를 지정할 수 없습니다는 [인라인](../../cpp/inline-functions-cpp.md) 지정자입니다. 컴파일러가 C4396 경고를 실행하고 인라인 지정자를 무시합니다.

### <a name="to-correct-this-error"></a>이 오류를 해결하려면

- friend 함수 선언에서 `inline`, `__inline`또는 `__forceinline` 지정자를 제거합니다.

## <a name="example"></a>예제

다음 코드 예제에서는 `inline` 지정자를 사용하는 잘못된 friend 함수 선언을 보여 줍니다.

```
// C4396.cpp
// compile with: /W2 /c

class X;
template<class T> void Func(T t, int i);

class X {
    friend inline void Func<char>(char t, int i);  //C4396
// try the following line instead
//    friend void Func<char>(char t, int i);
    int i;
};
```