---
title: 컴파일러 오류 C3919 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3919
dev_langs:
- C++
helpviewer_keywords:
- C3919
ms.assetid: 5f8eddda-d751-478b-930d-e18f7191ddfb
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 565146e714e0aa9a3598e4fe5fdeea361454ec78
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46136116"
---
# <a name="compiler-error-c3919"></a>컴파일러 오류 C3919

'event_method': 함수는 'type '형식이 있어야 합니다.

이벤트 접근자 메서드를 제대로 선언 되지 않았습니다.

이벤트에 대 한 자세한 내용은 참조 하세요. [이벤트](../../windows/event-cpp-component-extensions.md)합니다.

다음 샘플에서는 C3919 오류가 생성 됩니다.

```
// C3919.cpp
// compile with: /clr /c
using namespace System;
delegate void D(String^);
ref class R {
   event D^ e {
      int add(int);   // C3919
      int remove(int);   // C3919

      void add(D^);   // OK
      void remove(D^);   // OK
   }
};
```