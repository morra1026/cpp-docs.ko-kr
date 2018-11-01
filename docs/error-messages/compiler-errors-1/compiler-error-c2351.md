---
title: 컴파일러 오류 C2351
ms.date: 11/04/2016
f1_keywords:
- C2351
helpviewer_keywords:
- C2351
ms.assetid: 5439ccf6-66f6-4859-964c-c73f5eddfc1b
ms.openlocfilehash: 2d93902ee0008a54da1b2ecf165e0a829362511f
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50665493"
---
# <a name="compiler-error-c2351"></a>컴파일러 오류 C2351

사용 되지 않는 c + + 생성자 초기화 구문입니다.

생성자에 대 한 새 스타일 초기화 목록에서 명시적으로 이름을 지정 해야 합니다 각 직접 기본 클래스에만 기본 클래스인 경우에 합니다.

다음 샘플에서는 C2351 오류가 생성 됩니다.

```
// C2351.cpp
// compile with: /c
class B {
public:
   B() : () {}   // C2351
   B() {}   // OK
};
```