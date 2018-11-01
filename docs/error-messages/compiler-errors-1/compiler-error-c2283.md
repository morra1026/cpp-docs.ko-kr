---
title: 컴파일러 오류 C2283
ms.date: 11/04/2016
f1_keywords:
- C2283
helpviewer_keywords:
- C2283
ms.assetid: 8a5b3175-b480-4598-a1f7-0b50504c5caa
ms.openlocfilehash: 1113236680241a80c462e382c8c9c7de342b5463
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50629998"
---
# <a name="compiler-error-c2283"></a>컴파일러 오류 C2283

'identifier': 순수 지정자 또는 추상 재정의 지정자는 명명되지 않은 struct에 사용할 수 없습니다.

명명되지 않은 클래스 또는 구조체의 멤버 함수가 허용되지 않는 순수 지정자를 사용하여 선언됩니다.

다음 샘플에서는 C2283을 생성합니다.

```
// C2283.cpp
// compile with: /c
struct {
   virtual void func() = 0;   // C2283
};
struct T {
   virtual void func() = 0;   // OK
};
```