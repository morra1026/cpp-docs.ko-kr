---
title: 컴파일러 오류 C2971
ms.date: 11/04/2016
f1_keywords:
- C2971
helpviewer_keywords:
- C2971
ms.assetid: fdb5467b-9a41-41ef-ac20-2e9428d5a4fc
ms.openlocfilehash: 09f3578bff5806fc32a3b5599dcfa8caa3696974
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50437299"
---
# <a name="compiler-error-c2971"></a>컴파일러 오류 C2971

'class': 템플릿 매개 변수 'param': 'arg': 지역 변수는 비형식 인수로 사용할 수 없습니다

이름 또는 지역 변수의 주소를 템플릿 인수로 사용할 수 없습니다.

다음 샘플에서는 C2971 오류가 생성 됩니다.

```
// C2971.cpp
template <int *pi>
class Y {};

int global_var = 0;

int main() {
   int local_var = 0;
   Y<&local_var> aY;   // C2971
   // try the following line instead
   // Y<&global_var> aY;
}
```