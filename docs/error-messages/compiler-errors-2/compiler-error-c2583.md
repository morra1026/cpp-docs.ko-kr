---
title: 컴파일러 오류 C2583 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2583
dev_langs:
- C++
helpviewer_keywords:
- C2583
ms.assetid: b1c952dc-872c-47e4-9fc8-4dd72bcee6f9
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 3aad4a818d0c8869681f9a2f4c4ace0edb63cd02
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46117532"
---
# <a name="compiler-error-c2583"></a>컴파일러 오류 C2583

'identifier': ' const/volatile ' 'this'이 포인터가 생성자/소멸자에 대해 잘못 되었습니다.

생성자 나 소멸자를 선언 `const` 또는 `volatile`합니다. 이것은 허용되지 않습니다.

다음 샘플에서는 C2583 오류가 생성 됩니다.

```
// C2583.cpp
// compile with: /c
class A {
public:
   int i;
   A() const;   // C2583

   // try the following line instead
   // A();
};
```