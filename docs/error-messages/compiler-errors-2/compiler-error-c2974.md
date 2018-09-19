---
title: 컴파일러 오류 C2974 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2974
dev_langs:
- C++
helpviewer_keywords:
- C2974
ms.assetid: 1b444260-f2bf-48d7-ab1e-35573d8c4a0e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 478639ee1eccf841361e8e7e880ac33669d69e1e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46100487"
---
# <a name="compiler-error-c2974"></a>컴파일러 오류 C2974

잘못 된 형식 인수 'number' 형식이 예상

제네릭 또는 템플릿 인수는 제네릭 또는 템플릿 선언을 일치 하지 않습니다. 형식 꺾쇠 괄호 안에 표시 됩니다. 올바른 유형을 검색 하는 제네릭 또는 템플릿 정의 확인 합니다.

다음 샘플에서는 C2974를 생성합니다.

```
// C2974.cpp
// C2974 expected
template <class T>
struct TC {};

template <typename T>
void tf(T){}

int main() {
   // Delete the following 2 lines to resolve
   TC<1>* tc;
   tf<"abc">("abc");

   TC<int>* tc;
   tf<const char *>("abc");
}
```

C2974는 제네릭을 사용할 때도 발생할 수 있습니다.

```
// C2974b.cpp
// compile with: /clr
// C2974 expected
using namespace System;
generic <class T>
ref struct GCtype {};

generic <typename T>
void gf(T){}

int main() {
   // Delete the following 2 lines to resolve
   GCtype<"a">^ gc;
   gf<"a">("abc");

   // OK
   GCtype<int>^ gc;
   gf<String ^>("abc");
}
```