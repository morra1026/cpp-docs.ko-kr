---
title: 컴파일러 오류 C2385 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2385
dev_langs:
- C++
helpviewer_keywords:
- C2385
ms.assetid: 6d3dd1f2-e56d-49d7-865c-6a9acdb17417
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a52a932d45c94fb63f3d7b943b2cd78fa1862e4f
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46029054"
---
# <a name="compiler-error-c2385"></a>컴파일러 오류 C2385

'member' 액세스가 모호 합니다

멤버 (둘 이상의 개체에서 상속 된) 둘 이상의 개체에서 파생 될 수 있습니다.  이 오류를 해결 하려면

- 캐스트를 통해 모호 하지 않은 멤버를 확인 합니다.

- 모호한 기본 클래스 멤버를 이름을 바꿉니다.

## <a name="example"></a>예제

다음 샘플 C2385를 생성합니다.

```
// C2385.cpp
// C2385 expected
#include <stdio.h>

struct A
{
    void x(int i)
    {
        printf_s("\nIn A::x");
    }
};

struct B
{
    void x(char c)
    {
        printf_s("\nIn B::x");
    }
};

// Delete the following line to resolve.
struct C : A, B {}

// Uncomment the following 4 lines to resolve.
// struct C : A, B
// {
//     using B::x;
//     using A::x;
// };

int main()
{
    C aC;
    aC.x(100);
    aC.x('c');
}

struct C : A, B
{
    using B::x;
    using A::x;
};
```