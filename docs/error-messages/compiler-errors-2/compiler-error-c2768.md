---
title: 컴파일러 오류 C2768
ms.date: 11/04/2016
f1_keywords:
- C2768
helpviewer_keywords:
- C2768
ms.assetid: a7f6047a-6a80-4737-ad5c-c12868639fb5
ms.openlocfilehash: 9c0fb8fb0a98830aaf061ba980e7bdd7903f25e1
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50626176"
---
# <a name="compiler-error-c2768"></a>컴파일러 오류 C2768

'function': 명시적 템플릿 인수를 잘못 사용 했습니다.

컴파일러가 함수 정의 함수 템플릿의 명시적 특수화로 간주 되었습니다 또는 함수 정의 된 새 함수에 있어야 할 경우를 결정할 수 없습니다.

이 오류는 Visual Studio.NET 2003에서 컴파일러 규칙 향상의 일부로 도입 되었습니다.

다음 샘플에서는 C2768 오류가 생성 됩니다.

```
// C2768.cpp
template<typename T>
void f(T) {}

void f<int>(int) {}   // C2768

// an explicit specialization
template<>
void f<int>(int) {}

// global nontemplate function overload
void f(int) {}
```