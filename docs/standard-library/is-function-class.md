---
title: is_function 클래스
ms.date: 11/04/2016
f1_keywords:
- type_traits/std::is
helpviewer_keywords:
- is_function class
- is
ms.assetid: e5c0dbcd-829b-415f-853f-8c5be47c5040
ms.openlocfilehash: 0d2559ca6d864a23c5949bcddee8790df4b2bb65
ms.sourcegitcommit: afd6fac7c519dbc47a4befaece14a919d4e0a8a2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/10/2018
ms.locfileid: "51523046"
---
# <a name="isfunction-class"></a>is_function 클래스

형식이 함수 형식인지 테스트합니다.

## <a name="syntax"></a>구문

```cpp
template <class Ty>
struct is_function;
```

### <a name="parameters"></a>매개 변수

*Ty*<br/>
형식이 쿼리입니다.

## <a name="remarks"></a>설명

형식 조건자의 인스턴스 형태인 경우 true 형식을 *Ty* 함수 형식, 그렇지 않으면 false입니다.

## <a name="example"></a>예제

```cpp
// std__type_traits__is_function.cpp
// compile with: /EHsc
#include <type_traits>
#include <iostream>

struct trivial
    {
    int val;
    };

struct functional
    {
    int f();
    };

int main()
    {
    std::cout << "is_function<trivial> == " << std::boolalpha
        << std::is_function<trivial>::value << std::endl;
    std::cout << "is_function<functional> == " << std::boolalpha
        << std::is_function<functional>::value << std::endl;
    std::cout << "is_function<float()> == " << std::boolalpha
        << std::is_function<float()>::value << std::endl;

    return (0);
    }
```

```Output
is_function<trivial> == false
is_function<functional> == false
is_function<float()> == true
```

## <a name="requirements"></a>요구 사항

**헤더:** \<type_traits>

**네임스페이스:** std

## <a name="see-also"></a>참고자료

[<type_traits>](../standard-library/type-traits.md)<br/>
[is_object 클래스](../standard-library/is-object-class.md)<br/>
