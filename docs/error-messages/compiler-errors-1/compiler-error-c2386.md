---
title: 컴파일러 오류 C2386
ms.date: 11/04/2016
f1_keywords:
- C2386
helpviewer_keywords:
- C2386
ms.assetid: aaaa1284-34a0-4da2-8547-9fcbb559dae0
ms.openlocfilehash: a75ccd9824106f2b954cd090a0e00ab11786d243
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50667660"
---
# <a name="compiler-error-c2386"></a>컴파일러 오류 C2386

'symbol': 이름이 같은 기호가 현재 범위에 이미 있습니다.

네임스페이스 별칭을 만들려고 했지만 선택한 이름이 이미 있습니다.

다음 샘플에서는 C2386을 생성합니다.

```
// C2386.cpp
namespace A {
   int k;
}

int i;
namespace i = A;   // C2386, i already exists
```