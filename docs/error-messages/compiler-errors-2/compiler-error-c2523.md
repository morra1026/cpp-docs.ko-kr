---
title: 컴파일러 오류 C2523 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2523
dev_langs:
- C++
helpviewer_keywords:
- C2523
ms.assetid: 7951b700-8f37-45a0-beb4-a79ae0ced72e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 77f440bf282d6159af3a96bfeb1aa7db8941e87b
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46022801"
---
# <a name="compiler-error-c2523"></a>컴파일러 오류 C2523

' 클래스:: ~ identifier': 소멸자/종료자 태그 일치 하지 않습니다.

소멸자 이름은 앞에 물결표 클래스 이름 이어야 합니다 (`~`). 생성자와 소멸자는 클래스와 동일한 이름을 가진 멤버만 있습니다.

다음 샘플에서는 C2523 오류가 생성 됩니다.

```
// C2523.cpp
// compile with: /c
class A {
   ~B();    // C2523
   ~A();   // OK
};
```