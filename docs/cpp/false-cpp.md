---
title: false (C++)
ms.date: 11/04/2016
f1_keywords:
- false_cpp
helpviewer_keywords:
- false keyword [C++]
ms.assetid: cc13aec5-1f02-4d38-8dbf-5473ea2b354f
ms.openlocfilehash: 5fc27c7f1dfde7d1f686f0a752652773ade9cc0e
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50464066"
---
# <a name="false-c"></a>false (C++)

키워드를 사용 하면 형식의 변수에 대 한 두 값 중 하나인 [bool](../cpp/bool-cpp.md) 조건식 (조건식은 이제는 **true** 부울 식). 예를 들어 경우 `i` 형식의 변수가 **bool**의 `i = false;` 문 할당 **false** 를 `i`합니다.

## <a name="example"></a>예제

```cpp
// bool_false.cpp
#include <stdio.h>

int main()
{
    bool bb = true;
    printf_s("%d\n", bb);
    bb = false;
    printf_s("%d\n", bb);
}
```

```Output
1
0
```

## <a name="see-also"></a>참고자료

[키워드](../cpp/keywords-cpp.md)