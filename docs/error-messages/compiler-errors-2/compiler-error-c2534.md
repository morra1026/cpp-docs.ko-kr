---
title: 컴파일러 오류 C2534
ms.date: 11/04/2016
f1_keywords:
- C2534
helpviewer_keywords:
- C2534
ms.assetid: 481f9f54-5b51-4aa0-8eea-218f10807705
ms.openlocfilehash: e684804ea31b16f31c82e244cb4f9a6aaf2d08c3
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50638258"
---
# <a name="compiler-error-c2534"></a>컴파일러 오류 C2534

'identifier': 생성자는 값을 반환할 수 없습니다.

생성자 값을 반환 하거나 반환 형식을 가질 수 없습니다 (갖추기를 `void` 반환 형식).

제거 하 여이 오류를 해결할 수 있습니다는 `return` 생성자 정의에서 문입니다.

다음 샘플에서는 C2534를 생성합니다.

```
// C2534.cpp
class A {
public:
   int i;
   A() { return i; }   // C2534
};
```