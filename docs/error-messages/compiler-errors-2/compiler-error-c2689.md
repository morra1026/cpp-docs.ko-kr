---
title: 컴파일러 오류 C2689 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2689
dev_langs:
- C++
helpviewer_keywords:
- C2689
ms.assetid: b5216fba-524d-4194-9168-26e9dc5210ce
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: fedb865a1c0c6e1bbefc94c03549936951b84e17
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46099894"
---
# <a name="compiler-error-c2689"></a>컴파일러 오류 C2689

'function': 지역 클래스 내에서 friend 함수를 정의할 수 없습니다

선언할 수 있지만 로컬 클래스의 friend 함수를 정의 하지 않습니다.

다음 샘플에서는 C2689 오류가 생성 됩니다.

```
// C2689.cpp
// compile with: /c
void g() {
   void f2();
   class X {
      friend void f2(){}   // C2689
      friend void f2();   // OK
   };
}
```