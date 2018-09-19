---
title: 컴파일러 오류 C3911 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3911
dev_langs:
- C++
helpviewer_keywords:
- C3911
ms.assetid: b786da59-0e99-479d-bc0d-551126e940f2
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 98b2b1b4712d71c5baa7179ce3c348ace3761bb2
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46037387"
---
# <a name="compiler-error-c3911"></a>컴파일러 오류 C3911

'event_accessor_method': 함수에는 형식 '서명' 있어야 합니다.

이벤트의 접근자 메서드를 제대로 선언 되지 않았습니다.

자세한 내용은 [이벤트](../../windows/event-cpp-component-extensions.md)합니다.

다음 샘플에서는 C3911 오류가 생성 됩니다.

```
// C3911.cpp
// compile with: /clr
using namespace System;
delegate void H(String^, int);

ref class X {
   event H^ E1 {
      void add() {}   // C3911
      // try the following line instead
      // void add(H ^ h) {}

      void remove(){}
      // try the following line instead
      // void remove(H ^ h) {}

      void raise(){}
      // try the following line instead
      // void raise(String ^ s, int i) {}
   };
};
```