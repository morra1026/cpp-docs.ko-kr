---
title: 컴파일러 오류 C2050 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2050
dev_langs:
- C++
helpviewer_keywords:
- C2050
ms.assetid: 66aaed7d-00db-4ce1-a9d6-4447c1cf07ce
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f3bae3c9478d83693ecab77cdde724a1f0ef6772
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46106027"
---
# <a name="compiler-error-c2050"></a>컴파일러 오류 C2050

switch 식이 정수 계열이 아닙니다

`switch` 정수가 아닌 값으로 계산 되는 식입니다. 이 오류를 해결 하려면 switch 문에서 정수 계열 값만을 사용 합니다.

다음 샘플에서는 C2050 오류가 생성 됩니다.

```
// C2050.cpp
int main() {
   int a = 1;
   switch ("a") {   // C2050
      case 1:
         a = 0;
      default:
         a = 2;
   }
}
```

해결 방법:

```
// C2050b.cpp
int main() {
   int a = 1;
   switch (a) {
      case 1:
         a = 0;
      default:
         a = 2;
   }
}
```