---
title: 컴파일러 오류 C2333
ms.date: 11/04/2016
f1_keywords:
- C2333
helpviewer_keywords:
- C2333
ms.assetid: 2636fc1e-d3e7-4e68-8628-3c81a99ba813
ms.openlocfilehash: e9119a8375a276a59cbf3a6db9541f6ccaef5122
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50432635"
---
# <a name="compiler-error-c2333"></a>컴파일러 오류 C2333

'function': 함수 선언; 하는 동안 오류가 발생 했습니다. 함수 본문을 건너뜁니다.

이 오류는 해당 클래스 내에서 정의 된 멤버 함수에 대 한 다른 오류가 발생 한 후 발생 합니다.

다음 샘플에서는 C2333 오류가 생성 됩니다.

```
// C2333.cpp
struct s1 {
   s1(s1) {}   // C2333
};
```