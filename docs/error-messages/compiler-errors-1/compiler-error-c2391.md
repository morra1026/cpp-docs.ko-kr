---
title: 컴파일러 오류 C2391 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2391
dev_langs:
- C++
helpviewer_keywords:
- C2391
ms.assetid: 63a9c6b9-03cc-4517-885c-bdcd048643b3
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 1201651ffc52dae7b8f184895f8005750ee4697e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46102374"
---
# <a name="compiler-error-c2391"></a>컴파일러 오류 C2391

'identifier': 형식 정의 하는 동안 'friend'를 사용할 수 없습니다

`friend` 선언이 완전 한 클래스 선언을 포함 합니다. `friend` 멤버 함수 또는 상세 형식 지정자, 하지만 완전 한 클래스 선언 되지 선언을 지정할 수 있습니다.

다음 샘플에서는 C2326을 생성합니다.

```
// C2391.cpp
// compile with: /c
class D {
   void func( int );
};

class A {
   friend class B { int i; };   // C2391

   // OK
   friend class C;
   friend void D::func(int);
};
```