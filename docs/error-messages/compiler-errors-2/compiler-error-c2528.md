---
title: 컴파일러 오류 C2528
ms.date: 11/04/2016
f1_keywords:
- C2528
helpviewer_keywords:
- C2528
ms.assetid: 2ea9d583-67a8-4b16-b35f-a50eeffc03c4
ms.openlocfilehash: 890dae7aa34103bde0168f1933bb42343d84100b
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50601749"
---
# <a name="compiler-error-c2528"></a>컴파일러 오류 C2528

'name': 참조 한 포인터가 잘못 되었습니다

참조에 대 한 포인터를 선언할 수 없습니다. 에 대 한 포인터를 선언 하기 전에 변수를 역참조 합니다.

다음 샘플에서는 C2528 오류가 생성 됩니다.

```
// C2528.cpp
int i;
int &ir = i;
int & (*irptr) = ir;    // C2528
```