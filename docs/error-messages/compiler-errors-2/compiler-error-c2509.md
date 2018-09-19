---
title: 컴파일러 오류 C2509 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2509
dev_langs:
- C++
helpviewer_keywords:
- C2509
ms.assetid: 339c1fcd-ec4a-456c-9f18-a9b24d9921af
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 7870ce7d1959ed849542f01c15ce647de472575e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46108335"
---
# <a name="compiler-error-c2509"></a>컴파일러 오류 C2509

'identifier': 'class'에서 선언 되지 멤버 함수

함수는 지정된 된 클래스에서 선언 되지 않았습니다.

## <a name="example"></a>예제

다음 샘플 C2509를 생성합니다.

```
// C2509.cpp
// compile with: /c
struct A {
   virtual int vfunc() = 0;
   virtual int vfunc2() = 0;
};

struct B : private A {
   using A::vfunc;
   virtual int vfunc2();
};

int B::vfunc() { return 1; }   // C2509
int B::vfunc2() { return 1; }   // OK
```