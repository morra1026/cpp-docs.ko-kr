---
title: 컴파일러 오류 C2147
ms.date: 11/04/2016
f1_keywords:
- C2147
helpviewer_keywords:
- C2147
ms.assetid: d1adb3bf-7ece-4815-922c-ad7492fb6670
ms.openlocfilehash: 0a093bbbaf9cf9f72625226f949a27b681005c35
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50614489"
---
# <a name="compiler-error-c2147"></a>컴파일러 오류 C2147

구문 오류: 'identifier'는 새로운 키워드

식별자는 이제 언어에서 예약된 된 키워드를 사용 했습니다.

다음 샘플에서는 C2147 오류가 생성 됩니다.

```
// C2147.cpp
// compile with: /clr
int main() {
   int gcnew = 0;   // C2147
   int i = 0;   // OK
}
```