---
title: 컴파일러 오류 C3910 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3910
dev_langs:
- C++
helpviewer_keywords:
- C3910
ms.assetid: cfcbe620-b463-463b-95ea-2d60ad33ebb5
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: dc5a719cac97a16ef6b8eaff277a9526a2f135ad
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46073839"
---
# <a name="compiler-error-c3910"></a>컴파일러 오류 C3910

'event': 'method' 멤버를 정의 해야 합니다

이벤트를 정의 되었지만 지정 된 필수 접근자 메서드가 없습니다.

자세한 내용은 [이벤트](../../windows/event-cpp-component-extensions.md)합니다.

다음 샘플에서는 C3910 오류가 생성 됩니다.

```
// C3910.cpp
// compile with: /clr /c
delegate void H();
ref class X {
   event H^ E {
      // uncomment the following lines
      // void add(H^) {}
      // void remove( H^ h ) {}
      // void raise( ) {}
   };   // C3910

   event H^ E2; // OK data member
};
```