---
title: alignof 및 alignas (c + +) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
ms.assetid: 1d18aa8a-9621-4fb5-86e5-4cc86d5187f4
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 96dd03d8aebb8860d5a16c8d08bb35dd8a7d8b48
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46065805"
---
# <a name="alignof-and-alignas-c"></a>alignof 및 alignas(C++)

합니다 **alignas** 형식 지정자는 변수 및 사용자 정의 형식의 사용자 지정 맞춤을 지정 하는 이식 가능 하며 c + + 표준 방법입니다. 합니다 **alignof** 연산자는 마찬가지로 표준, 이식 가능한 방법 지정 된 형식 또는 변수의 맞춤을 가져옵니다.

## <a name="example"></a>예제

사용할 수 있습니다 **alignas** 구조체 / 공용 구조체, 클래스 또는 개별 멤버입니다. 때 여러 **alignas** 지정자 발생 하는, 컴파일러는 엄격한 것 (가장 큰 값을 사용 하 여 하나)를 선택 합니다.

```cpp
// alignas_alignof.cpp
// compile with: cl /EHsc alignas_alignof.cpp
#include <iostream>

struct alignas(16) Bar
{
    int i;       // 4 bytes
    int n;      // 4 bytes
    alignas(4) char arr[3];
    short s;          // 2 bytes
};

int main()
{
    std::cout << alignof(Bar) << std::endl; // output: 16
}
```

## <a name="see-also"></a>참고자료

[맞춤](../cpp/alignment-cpp-declarations.md)