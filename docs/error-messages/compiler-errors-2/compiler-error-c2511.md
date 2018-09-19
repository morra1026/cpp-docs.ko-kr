---
title: 컴파일러 오류 C2511 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2511
dev_langs:
- C++
helpviewer_keywords:
- C2511
ms.assetid: df999efe-fe2b-418b-bb55-4af6a0592631
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b628adda383baee0f2ec03ace715d94c6cca764c
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46058148"
---
# <a name="compiler-error-c2511"></a>컴파일러 오류 C2511

'identifier': 오버 로드 된 멤버 함수가 'class'에서 찾을 수 없습니다

함수의 버전이 지정된 된 매개 변수를 사용 하 여 선언 됩니다.  가능한 원인:

1. 잘못 된 매개 변수는 함수에 전달 합니다.

1. 매개 변수가 잘못 된 순서 대로 전달 합니다.

1. 매개 변수 이름의 철자가 잘못 되었습니다.

다음 샘플에서는 C2511을 생성합니다.

```
// C2511.cpp
// compile with: /c
class C {
   int c_2;
   int Func(char *, char *);
};

int C::Func(char *, char *, int i) {   // C2511
// try the following line instead
// int C::Func(char *, char *) {
   return 0;
}
```