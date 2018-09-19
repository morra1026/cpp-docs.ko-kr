---
title: 컴파일러 오류 C2695 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2695
dev_langs:
- C++
helpviewer_keywords:
- C2695
ms.assetid: 3f6f2091-c38b-40ea-ab6c-f1846f5702d7
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a618c02fcf3a8927d8090b1ad51ed16d9ac28542
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46056055"
---
# <a name="compiler-error-c2695"></a>컴파일러 오류 C2695

'function1': 재정의 가상 함수에서 'function2'만 다른 호출 규칙

파생된 클래스에서 함수 서명의 기본 클래스의 함수를 재정의 및 호출 규칙을 변경할 수 없습니다.

다음 샘플에서는 C2695를 생성합니다.

```
// C2695.cpp
class C {
   virtual void __fastcall func();
};

class D : public C {
   virtual void __clrcall func();   // C2695
};
```