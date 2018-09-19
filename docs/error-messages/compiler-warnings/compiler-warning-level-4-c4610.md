---
title: 컴파일러 경고 (수준 4) C4610 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4610
dev_langs:
- C++
helpviewer_keywords:
- C4610
ms.assetid: 23c1a16c-9ca9-4bf6-9911-a72b785560c2
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 2f45b216f240b2c51382d6fd4054f2b959c19088
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46051570"
---
# <a name="compiler-warning-level-4-c4610"></a>컴파일러 경고(수준 4) C4610

'class' 개체를 인스턴스화할 수 없습니다-사용자 정의 생성자가 필요

가 없는 사용자 정의 클래스나 기본 생성자입니다. 없는 인스턴스화 수행 됩니다. 다음 샘플에서는 C4610 오류가 생성 됩니다.

```
// C4610.cpp
// compile with: /W4
struct A {
   int &j;

   A& A::operator=( const A& );
};   // C4610

/* use this structure definition to resolve the warning
struct B {
   int &k;

   B(int i = 0) : k(i) {
   }

   B& B::operator=( const B& );
} b;
*/

int main() {
}
```