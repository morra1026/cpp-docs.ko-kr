---
title: 컴파일러 오류 C3060 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3060
dev_langs:
- C++
helpviewer_keywords:
- C3060
ms.assetid: 6282bb92-0546-4b59-9435-d3840bf93bdb
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c053f7b92ae12b3e99792603cf7b3c5ac9b49227
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46108601"
---
# <a name="compiler-error-c3060"></a>컴파일러 오류 C3060

'member': friend 함수는 클래스 내부에서 정규화된 이름을 사용하여 정의할 수 없으며 선언만 할 수 있습니다.

Friend 함수가 정규화된 이름을 사용하여 정의되었으며 이는 허용되지 않습니다.

다음 샘플에서는 C3060을 생성합니다.

```
// C3060.cpp
class A {
public:
   void func();
};

class C {
public:
   friend void A::func() { }   // C3060
   // Try the following line and the out of class definition:
   // friend void A::func();
};

// void A::func(){}
```