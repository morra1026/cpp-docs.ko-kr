---
title: 컴파일러 오류 C2794 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2794
dev_langs:
- C++
helpviewer_keywords:
- C2794
ms.assetid: d508191c-9044-4c6a-9119-4bca668c0b93
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 4c81e8dcfde2a24c4a827406c3e499c12e891b2f
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46068015"
---
# <a name="compiler-error-c2794"></a>컴파일러 오류 C2794

'function': 'class' 모든 직접 또는 간접 기본 클래스의 멤버가 아닙니다.

사용 하려는 [super](../../cpp/super.md) 존재 하지 않는 멤버 함수를 호출 합니다.

다음 샘플에서는 C2794

```
// C2794.cpp
struct B {
   void mf();
};

struct D : B {
   void mf() {
      __super::f();  // C2794
   }
};
```