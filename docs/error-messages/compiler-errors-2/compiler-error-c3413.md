---
title: 컴파일러 오류 C3413
ms.date: 11/04/2016
f1_keywords:
- C3413
helpviewer_keywords:
- C3413
ms.assetid: de6c9b05-c373-4bd8-8cb0-12c2cd2e5674
ms.openlocfilehash: e344d06345c0f3a79b86e9cab4e1c5dacb47e9c2
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50453289"
---
# <a name="compiler-error-c3413"></a>컴파일러 오류 C3413

'name': 잘못된 명시적 인스턴스화입니다.

컴파일러가 잘못된 형식의 명시적 인스턴스화를 검색했습니다.

다음 샘플에서는 C3413을 생성합니다.

```
// C3413.cpp
template
class MyClass {};   // C3413
```

해결 방법:

```
// C3413b.cpp
// compile with: /c
template <class T>
class MyClass {};

template <>
class MyClass<int> {};
```