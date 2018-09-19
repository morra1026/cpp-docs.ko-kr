---
title: 컴파일러 오류 C2571 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2571
dev_langs:
- C++
helpviewer_keywords:
- C2571
ms.assetid: c6522616-dee9-4d7d-9bf8-30a7e1deaadf
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 30cc078251d0511da77e08690db275a788973ffb
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46067937"
---
# <a name="compiler-error-c2571"></a>컴파일러 오류 C2571

'function': ' union'에서 가상 함수 일 수 없습니다

공용 구조체는 가상 함수를 사용 하 여 선언 됩니다. 클래스 또는 구조체에만 가상 함수를 선언할 수 있습니다.  가능한 해결 방법:

1. 클래스 또는 구조체를 공용 구조체를 변경 합니다.

1. 비가상 함수를 확인 합니다.

다음 샘플에서는 C2571 오류가 생성 됩니다.

```
// C2571.cpp
// compile with: /c
union A {
   virtual void func1();   // C2571
   void func2();   // OK
};
```