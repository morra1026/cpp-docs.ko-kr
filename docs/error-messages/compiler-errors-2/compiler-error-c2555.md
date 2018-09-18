---
title: 컴파일러 오류 C2555 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2555
dev_langs:
- C++
helpviewer_keywords:
- C2555
ms.assetid: 5e49ebb8-7c90-457a-aa12-7ca7ab6574b2
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 8f91ec33db2d3a7b6772556233a3c99b501ede76
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46017341"
---
# <a name="compiler-error-c2555"></a>컴파일러 오류 C2555

'class1::function1': 재정의 가상 함수의 반환 형식이 다른 고 아닌 'class2::function2'에서 공변 (covariant)

가상 함수 및 파생된 재정의 함수에는 있지만 다른 반환 형식은 동일한 매개 변수 목록에 있습니다. 파생된 클래스에서 재정의 함수를 반환 형식에 의해서만 기본 클래스의 가상 함수에서 다를 수 없습니다.

이 오류를 해결 하려면 가상 함수를 호출한 후 반환 값을 캐스팅 합니다.

/Clr을 사용 하 여 컴파일하는 경우에이 오류가 나타날 수 있습니다.   예를 들어, Visual c + + 다음 C# 선언에 해당 합니다.

```
Guid[] CheckSources(Guid sourceID, Guid[] carouselIDs);
```

is

```
Guid CheckSources(Guid sourceID, Guid carouselIDs[]) [];
```

C2555에 대 한 자세한 내용은 기술 자료 문서 Q240862를 참조 하세요.

다음 샘플에서는 C2555 오류가 생성 됩니다.

```
// C2555.cpp
// compile with: /c
struct X {
   virtual void func();
};
struct Y : X {
   char func();  // C2555
   void func2();   // OK
};
```