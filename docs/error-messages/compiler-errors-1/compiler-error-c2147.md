---
title: 컴파일러 오류 C2147 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2147
dev_langs:
- C++
helpviewer_keywords:
- C2147
ms.assetid: d1adb3bf-7ece-4815-922c-ad7492fb6670
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 786d47e23986962575567b8afdc2eefd5aac5be6
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46082432"
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