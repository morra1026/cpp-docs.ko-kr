---
title: 컴파일러 오류 C2073 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2073
dev_langs:
- C++
helpviewer_keywords:
- C2073
ms.assetid: 57908234-be7a-4ce9-b0a7-8b1ad621865e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 950ca9551a605da392c1f033cb1784ff43a7fefc
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46112371"
---
# <a name="compiler-error-c2073"></a>컴파일러 오류 C2073

'identifier': 부분적으로 초기화 된 배열의 요소에는 기본 생성자가 있어야 합니다.

사용자 정의 형식 또는 상수 배열에 대 한 이니셜라이저를 너무 적게 지정 되었습니다. 배열 멤버에 대 한 명시적 이니셜라이저 및 해당 생성자는 지정 하지 않으면 기본 생성자를 제공 해야 합니다.

다음 샘플에서는 C2073 오류가 생성 됩니다.

```
// C2073.cpp
class A {
public:
   A( int );   // constructor for ints only
};
A a[3] = { A(1), A(2) };   // C2073, no default constructor
```

```
// C2073b.cpp
// compile with: /c
class B {
public:
   B();   // default constructor declared
   B( int );
};
B b[3] = { B(1), B(2) };   // OK
```