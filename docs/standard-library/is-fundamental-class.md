---
title: is_fundamental 클래스
ms.date: 11/04/2016
f1_keywords:
- type_traits/std::is_fundamental
helpviewer_keywords:
- is_fundamental class
- is_fundamental
ms.assetid: b84eee84-2fb2-4611-beaf-b384074d8b6a
ms.openlocfilehash: d16dfeebabd5909212425fcc27b355110e891d89
ms.sourcegitcommit: afd6fac7c519dbc47a4befaece14a919d4e0a8a2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/10/2018
ms.locfileid: "51524113"
---
# <a name="isfundamental-class"></a>is_fundamental 클래스

형식이 void 또는 산술형인지 테스트합니다.

## <a name="syntax"></a>구문

```cpp
template <class Ty>
struct is_fundamental;
```

### <a name="parameters"></a>매개 변수

*Ty*<br/>
형식이 쿼리입니다.

## <a name="remarks"></a>설명

형식 조건자의 인스턴스 형태인 경우 true 형식 *Ty* 즉,이 기본 형식이 **void**, 정수 형식, 부동 소수점 형식 또는 `cv-qualified` 고, 그렇지 않으면 false 중 하나의 형식을 합니다.

## <a name="example"></a>예제

```cpp
// std__type_traits__is_fundamental.cpp
// compile with: /EHsc
#include <type_traits>
#include <iostream>

struct trivial
    {
    int val;
    };

int main()
    {
    std::cout << "is_fundamental<trivial> == " << std::boolalpha
        << std::is_fundamental<trivial>::value << std::endl;
    std::cout << "is_fundamental<int> == " << std::boolalpha
        << std::is_fundamental<int>::value << std::endl;
    std::cout << "is_fundamental<const float> == " << std::boolalpha
        << std::is_fundamental<const float>::value << std::endl;
    std::cout << "is_fundamental<void> == " << std::boolalpha
        << std::is_fundamental<void>::value << std::endl;

    return (0);
    }
```

```Output
is_fundamental<trivial> == false
is_fundamental<int> == true
is_fundamental<const float> == true
is_fundamental<void> == true
```

## <a name="requirements"></a>요구 사항

**헤더:** \<type_traits>

**네임스페이스:** std

## <a name="see-also"></a>참고자료

[<type_traits>](../standard-library/type-traits.md)<br/>
[is_compound 클래스](../standard-library/is-compound-class.md)<br/>
