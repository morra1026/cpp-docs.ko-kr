---
title: 컴파일러 오류 C2514 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2514
dev_langs:
- C++
helpviewer_keywords:
- C2514
ms.assetid: 4b7085e5-6714-4261-80b7-bc72e64ab3e8
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 392c46224078c35df5ae02a88503726b193c87f3
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46085513"
---
# <a name="compiler-error-c2514"></a>컴파일러 오류 C2514

'class': 클래스에 생성자가 없습니다

클래스, 구조체 또는 공용 구조체에 생성자를 없습니다 인스턴스화해야 하는 데 사용 되는 매개 변수와 일치 하는 매개 변수 목록 사용 합니다.

클래스를 인스턴스화하려면 먼저 완벽 하 게 선언 되어야 합니다.

다음 샘플에서는 C2514를 생성합니다.

```
// C2514.cpp
// compile with: /c
class f;

class g {
public:
    g (int x);
};

class fmaker {
   f *func1() {
      return new f(2);   // C2514
   }

   g *func2() {
      return new g(2);   // OK
   }
};
```