---
title: 컴파일러 오류 C2273
ms.date: 11/04/2016
f1_keywords:
- C2273
helpviewer_keywords:
- C2273
ms.assetid: 3c682c66-97bf-4a23-a22c-d9a26a92bf95
ms.openlocfilehash: f2ed5c49a9f8243fd5c9c302caf2876493c26bc3
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50526396"
---
# <a name="compiler-error-c2273"></a>컴파일러 오류 C2273

'type': '->' 연산자의 오른쪽에 사용할 수 없습니다.

오른쪽 피연산자로 형식이 표시를 `->` 연산자입니다.

이 오류는 사용자 정의 형식 변환에 액세스 하려고 시도 하 여 발생할 수 있습니다. ->와 `operator` 사이에 `type` 키워드를 사용하십시오.

다음 샘플에서는 C2273를 생성합니다.

```
// C2273.cpp
struct MyClass {
   operator int() {
      return 0;
   }
};
int main() {
   MyClass * ClassPtr = new MyClass;
   int i = ClassPtr->int();   // C2273
   int j = ClassPtr-> operator int();   // OK
}
```