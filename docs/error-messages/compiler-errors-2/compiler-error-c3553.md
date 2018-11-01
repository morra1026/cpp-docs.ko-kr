---
title: 컴파일러 오류 C3553
ms.date: 11/04/2016
f1_keywords:
- C3553
helpviewer_keywords:
- C3553
ms.assetid: 7f84bf37-6419-4ad3-ab30-64266100b930
ms.openlocfilehash: 219592f2403904f9923e84bfd4539a22cddd02de
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50543431"
---
# <a name="compiler-error-c3553"></a>컴파일러 오류 C3553

> decltype에 형식이 아니라 식이 필요합니다.

`decltype()` 키워드는 형식 이름이 아니다를 인수로 식을 사용하도록 요구합니다. 예를 들어 다음 코드 조각의 마지막 문은 C3553 오류를 생성합니다.

```cpp
int x = 0;
decltype(x+1);
decltype(int); // C3553
```