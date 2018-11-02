---
title: 컴파일러 오류 C2947
ms.date: 11/04/2016
f1_keywords:
- C2947
helpviewer_keywords:
- C2947
ms.assetid: 6c056f62-ec90-4883-8a67-aeeb6ec13546
ms.openlocfilehash: 3738c257192134eedb8554b0d875023862441416
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50566762"
---
# <a name="compiler-error-c2947"></a>컴파일러 오류 C2947

construct을(를) 끝내려면 '>' 기호가 있어야 하는데 'syntax'이(가) 있습니다.

제네릭 또는 템플릿 인수 목록은 올바르게 종료 되지 않을 수 있습니다.

구문 오류로 인해 C2947 생성할 수도 있습니다.

다음 샘플에서는 C2947 오류가 생성 됩니다.

```
// C2947.cpp
// compile with: /c
template <typename T>=   // C2947
// try the following line instead
// template <typename T>
struct A {};
```