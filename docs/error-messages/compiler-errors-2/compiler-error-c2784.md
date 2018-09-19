---
title: 컴파일러 오류 C2784 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2784
dev_langs:
- C++
helpviewer_keywords:
- C2784
ms.assetid: 3d761fe2-881c-48bd-afae-e2e714e20473
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ed0e5dd7628031a7ad5ac66d2b691ee52dda62f2
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46091311"
---
# <a name="compiler-error-c2784"></a>컴파일러 오류 C2784

'declaration': 'type'의 템플릿 인수를 'type'에서 추론할 수 없습니다.

컴파일러가 제공된 함수 인수에서 템플릿 인수를 확인할 수 없습니다.

다음 샘플에서는 C2784를 생성하고 해결 방법을 보여 줍니다.

```
// C2784.cpp
template<class T> class X {};
template<class T> void f(X<T>) {}

int main() {
   X<int> x;
   f(1);   // C2784

   // To fix it, try the following line instead
   f(x);
}
```