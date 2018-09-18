---
title: 컴파일러 경고 (수준 1) C4584 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4584
dev_langs:
- C++
helpviewer_keywords:
- C4584
ms.assetid: ad86582f-cb8c-4d21-8c4c-a6c800059e25
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 9db97bf35034f7ca628f860924bfb9a1fccc942f
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46036256"
---
# <a name="compiler-warning-level-1-c4584"></a>컴파일러 경고(수준 1) C4584

'class1': 기본 클래스 'class2' 이미 'class3'의 기본 클래스입니다.

클래스 정의에서 다른 상속 하는 중 두 개의 클래스에서 상속 됩니다. 예를 들어:

```
// C4584.cpp
// compile with: /W1 /LD
class A {
};

class B : public A {
};

class C : public A, public B { // C4584
};
```

이 경우에 경고가 발생 합니다. 클래스 C에 모두 클래스 A 및 B 또한 A. 클래스에서 상속 되는 클래스에서 상속 하므로 이 경고는 이러한 기본 클래스에서 멤버를 사용 하는 정규화 해야 하거나 참조 하는 클래스 멤버에 대 한 모호성으로 인해 컴파일러 오류를 생성할 알림으로 사용 됩니다.