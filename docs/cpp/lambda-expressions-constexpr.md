---
title: c + +에서 constexpr 람다 식
ms.date: 07/19/2017
helpviewer_keywords:
- lambda expressions [C++], constexpr
ms.assetid: b56346cd-fbff-475f-aeaa-ed2010c6d6f7
ms.openlocfilehash: 937fae7da0f20e81ac5450d597af7a822219d654
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50506602"
---
# <a name="constexpr-lambda-expressions-in-c"></a>c + +에서 constexpr 람다 식

**Visual Studio 2017 15.3버전 이상** (컴파일 옵션 [/std:c++17](../build/reference/std-specify-language-standard-version.md)와 함께 사용 가능): 람다식은 **constexpr**로 선언되거나 캡처되거나 상수 내에서 각 데이터 맴버의 초기화가 허용되는 경우 상수식에 사용됩니다.

```cpp
    int y = 32;
    auto answer = [y]() constexpr
    {
        int x = 10;
        return y + x;
    };

    constexpr int Increment(int n)
    {
        return [n] { return n + 1; }();
    }
```

람다는 결과가 **constexpr**함수의 요구사항을 만족하면 암시적으로 **constexpr**가 됩니다.

```cpp
    auto answer = [](int n)
    {
        return 32 + n;
    };

    constexpr int response = answer(10);
```

람다는 암시적 혹은 명시적으로도 **constexpr**이고, 함수 포인터로 변환하면 결과 함수도 **constexpr**입니다.

```cpp
    auto Increment = [](int n)
    {
        return n + 1;
    };

    constexpr int(*inc)(int) = Increment;
```

## <a name="see-also"></a>참고자료

[C++ 언어 참조](../cpp/cpp-language-reference.md)<br/>
[C++ 표준 라이브러리의 함수 개체](../standard-library/function-objects-in-the-stl.md)<br/>
[함수 호출](../cpp/function-call-cpp.md)<br/>
[for_each](../standard-library/algorithm-functions.md#for_each)