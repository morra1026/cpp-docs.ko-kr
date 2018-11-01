---
title: 컴파일러 오류 C3264
ms.date: 11/04/2016
f1_keywords:
- C3264
helpviewer_keywords:
- C3264
ms.assetid: 94ece687-2364-4f7a-8ebb-7afd3ae9d63d
ms.openlocfilehash: 2f5a58335a36affc73deb490c9423284852ecbab
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50537529"
---
# <a name="compiler-error-c3264"></a>컴파일러 오류 C3264

'class': 클래스-생성자는 반환 형식을 가질 수 없습니다.

클래스 생성자가 반환 형식을 가질 수 없습니다.

다음 샘플에서는 C3264를 생성합니다.

```
// C3264_2.cpp
// compile with: /clr

ref class X {
   public:
      static int X()   { // C3264
      }

      /* use the code below to resolve the error
      static X() {
      }
      */
};
int main() {
}
```
