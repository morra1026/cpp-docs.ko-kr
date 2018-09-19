---
title: 컴파일러 오류 C3866 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3866
dev_langs:
- C++
helpviewer_keywords:
- C3866
ms.assetid: 685870af-2440-4cdf-a6cb-284a5b96ef9d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: eb56440dd67bc59e7719acdf70cee2784c889db2
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46048905"
---
# <a name="compiler-error-c3866"></a>컴파일러 오류 C3866

인수 목록이 없습니다. 함수 호출

비정적 멤버 함수 내에 종료자 또는 소멸자를 호출 하며 인수 목록의 아닙니다.

다음 샘플에서는 C3866 오류가 생성 됩니다.

```
// C3866.cpp
// compile with: /c
class C {
   ~C();
   void f() {
      this->~C;   // C3866
      this->~C();   // OK
   }
};
```