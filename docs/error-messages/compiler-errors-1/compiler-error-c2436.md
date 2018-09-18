---
title: 컴파일러 오류 C2436 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2436
dev_langs:
- C++
helpviewer_keywords:
- C2436
ms.assetid: ca4cc813-bc1d-4c0a-9a2c-3a5fe673d084
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f32b94f0e68de893897a5bdf48977a47417e6729
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46032993"
---
# <a name="compiler-error-c2436"></a>컴파일러 오류 C2436

'identifier': 멤버 함수 또는 생성자 이니셜라이저 목록에서 중첩된 클래스

멤버 함수 또는 생성자 이니셜라이저 목록에서 로컬 클래스를 초기화할 수 없습니다.

다음 샘플에서는 C2436 오류가 생성 됩니다.

```
// C2436.cpp
struct S{
   int f();
   struct Inner{
      int i;
   };
   S():f(10), Inner(0){}   // C2436
};
```