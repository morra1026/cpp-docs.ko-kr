---
title: 컴파일러 오류 C2079 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2079
dev_langs:
- C++
helpviewer_keywords:
- C2079
ms.assetid: ca58d6d5-eccd-40b7-ba14-c003223c5bc7
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 9ddea9a8651a62f7cbb857e1d53962142471c2cb
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46032187"
---
# <a name="compiler-error-c2079"></a>컴파일러 오류 C2079

'identifier' 정의 되지 않은 클래스/구조체/공용 'name' 사용

지정된 된 식별자는 정의 되지 않은 클래스, 구조체 또는 공용 구조체는 합니다.

이 오류는 익명 공용 구조체를 초기화 하 여 발생할 수 있습니다.

다음 샘플에서는 C2079를 생성합니다.

```
// C2079.cpp
// compile with: /EHsc
#include <iostream>
int main() {
   std::ifstream g;   // C2079
}
```

해결 방법:

```
// C2079b.cpp
// compile with: /EHsc
#include <fstream>
int main( ) {
   std::ifstream g;
}
```

C2079 스택의 범위 에서만에서 정방향 선언이 해당 형식의 개체를 선언 하려고 시도 하는 경우에 발생할 수 있습니다.

```
// C2079c.cpp
class A;

class B {
   A a;   // C2079
};

class A {};
```

해결 방법:

```
// C2079d.cpp
// compile with: /c
class A;
class C {};

class B {
   A * a;
   C c;
};

class A {};
```