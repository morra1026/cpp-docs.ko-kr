---
title: add_lvalue_reference 클래스 | Microsoft 문서
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
f1_keywords:
- type_traits/std::add_lvalue_reference
dev_langs:
- C++
helpviewer_keywords:
- add_lvalue_reference
ms.assetid: 9933afc2-ad0d-465d-98fe-7d547fa3efe2
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 46ca75850aede04d54dc659e3f29166ab91abdbf
ms.sourcegitcommit: 761c5f7c506915f5a62ef3847714f43e9b815352
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44102631"
---
# <a name="addlvaluereference-class"></a>add_lvalue_reference 클래스

형식에서 형식에 대한 참조를 만듭니다.

## <a name="syntax"></a>구문

```cpp
template <class T>
struct add_lvalue_reference;

template <class T>
using add_lvalue_reference_t = typename add_lvalue_reference<T>::type;
```

### <a name="parameters"></a>매개 변수

*T*<br/>
수정할 형식입니다.

## <a name="remarks"></a>설명

형식 수정자의 인스턴스는 수정 된 형식인 됩니다 *T* 하는 경우 *T* lvalue 참조 인 라인인 `T&`합니다.

## <a name="example"></a>예제

```cpp
#include <type_traits>
#include <iostream>

using namespace std;
int main()
{
    int val = 0;
    add_lvalue_reference_t<int> p = (int&)val;
    p = p;  // to quiet "unused" warning
    cout << "add_lvalue_reference_t<int> == "
        << typeid(p).name() << endl;

    return (0);
}
```

```Output
add_lvalue_reference_t<int> == int
```

## <a name="requirements"></a>요구 사항

**헤더:** \<type_traits>

**네임스페이스:** std

## <a name="see-also"></a>참고자료

[<type_traits>](../standard-library/type-traits.md)<br/>
[remove_reference 클래스](../standard-library/remove-reference-class.md)<br/>
