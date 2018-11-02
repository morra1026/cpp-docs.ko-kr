---
title: 컴파일러 오류 C2110
ms.date: 11/04/2016
f1_keywords:
- C2110
helpviewer_keywords:
- C2110
ms.assetid: 48fd76ed-90d6-4a60-9c7b-f6ce9355b4ca
ms.openlocfilehash: b20e68ec032abdfae9afb1c94fed064010275149
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50646968"
---
# <a name="compiler-error-c2110"></a>컴파일러 오류 C2110

'+': 두 포인터를 더할 수 없습니다.

더하기( `+` ) 연산자를 사용하여 두 포인터 값을 더하려고 했습니다.

다음 샘플에서는 C2110을 생성합니다.

```
// C2110.cpp
int main() {
   int a = 0;
   int *pa;
   int *pb;
   a = pa + pb;   // C2110
}
```