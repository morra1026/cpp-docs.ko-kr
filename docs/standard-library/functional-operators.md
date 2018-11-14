---
title: '&lt;functional&gt; 연산자'
ms.date: 11/04/2016
f1_keywords:
- functional/std::operator!=
- functional/std::operator==
helpviewer_keywords:
- functional operators
ms.assetid: d4b3c760-f3e2-4b65-bdaa-d42e8dd6f5e1
ms.openlocfilehash: 6fd4e25b3ca7b56e2221cb99b64f7c8e109bf452
ms.sourcegitcommit: afd6fac7c519dbc47a4befaece14a919d4e0a8a2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/10/2018
ms.locfileid: "51521923"
---
# <a name="ltfunctionalgt-operators"></a>&lt;functional&gt; 연산자

|||
|-|-|
|[operator!=](#op_neq)|[연산자==](#op_eq_eq)|

## <a name="op_eq_eq"></a>  operator==

호출 가능 개체가 비어 있는지 테스트합니다.

```cpp
template <class Fty>
bool operator==(const function<Fty>& f, null_ptr_type npc);

template <class Fty>
bool operator==(null_ptr_type npc, const function<Fty>& f);
```

### <a name="parameters"></a>매개 변수

*Fty*<br/>
래핑할 함수 형식입니다.

*f*<br/>
함수 개체입니다.

*npc*<br/>
null 포인터입니다.

### <a name="remarks"></a>설명

연산자는 둘 다 `function` 개체에 대한 참조인 인수와 null 포인터 상수인 인수를 사용합니다. `function` 개체가 비어 있는 경우에만 둘 다 true를 반환합니다.

### <a name="example"></a>예제

```cpp
// std__functional__operator_eq.cpp
// compile with: /EHsc
#include <functional>
#include <iostream>

int neg(int val)
{
    return (-val);
}

int main()
{
    std::function<int(int)> fn0;
    std::cout << std::boolalpha << "empty == "
        << (fn0 == 0) << std::endl;

    std::function<int(int)> fn1(neg);
    std::cout << std::boolalpha << "empty == "
        << (fn1 == 0) << std::endl;

    return (0);
}
```

```Output
empty == true
empty == false
```

## <a name="op_neq"></a>  operator!=

호출 가능 개체가 비어 있지 않은지 테스트합니다.

```cpp
template <class Fty>
bool operator!=(const function<Fty>& f, null_ptr_type npc);

template <class Fty>
bool operator!=(null_ptr_type npc, const function<Fty>& f);
```

### <a name="parameters"></a>매개 변수

*Fty*<br/>
래핑할 함수 형식입니다.

*f*<br/>
함수 개체입니다.

*npc*<br/>
null 포인터입니다.

### <a name="remarks"></a>설명

연산자는 둘 다 `function` 개체에 대한 참조인 인수와 null 포인터 상수인 인수를 사용합니다. `function` 개체가 비어 있지 않은 경우에만 둘 다 true를 반환합니다.

### <a name="example"></a>예제

```cpp
// std__functional__operator_ne.cpp
// compile with: /EHsc
#include <functional>
#include <iostream>

int neg(int val)
    {
    return (-val);
    }

int main()
    {
    std::function<int (int)> fn0;
    std::cout << std::boolalpha << "not empty == "
        << (fn0 != 0) << std::endl;

    std::function<int (int)> fn1(neg);
    std::cout << std::boolalpha << "not empty == "
        << (fn1 != 0) << std::endl;

    return (0);
    }
```

```Output
not empty == false
not empty == true
```

## <a name="see-also"></a>참고자료

[\<functional>](../standard-library/functional.md)<br/>
