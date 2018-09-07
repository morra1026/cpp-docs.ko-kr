---
title: binder1st 클래스 | Microsoft 문서
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
f1_keywords:
- xfunctional/std::binder1st
dev_langs:
- C++
helpviewer_keywords:
- binder1st class
ms.assetid: 6b8ee343-c82f-48f8-867d-06f9d1d324c0
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a9e53d9344e56f9efc4f20b834ce31bcb05f9fbb
ms.sourcegitcommit: 761c5f7c506915f5a62ef3847714f43e9b815352
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44103988"
---
# <a name="binder1st-class"></a>binder1st 클래스

이항 함수의 첫 번째 인수를 지정된 값에 바인딩하여 이항 함수 개체를 단항 함수 개체로 변환하는 생성자를 제공하는 템플릿 클래스입니다.

## <a name="syntax"></a>구문

```cpp
template <class Operation>
class binder1st
    : public unaryFunction <typename Operation::second_argument_type,
                             typename Operation::result_type>
{
public:
    typedef typename Operation::argument_type argument_type;
    typedef typename Operation::result_type result_type;
    binder1st(
        const Operation& Func,
        const typename Operation::first_argument_type& left);

    result_type operator()(const argument_type& right) const;
    result_type operator()(const argument_type& right) const;

protected:
    Operation op;
    typename Operation::first_argument_type value;
};
```

### <a name="parameters"></a>매개 변수

*Func*<br/>
단항 함수 개체로 변환할 이항 함수 개체입니다.

*left*<br/>
이항 함수 개체의 첫 번째 인수가 바인딩되는 값입니다.

*right*<br/>
수정된 이진 개체를 두 번째 인수의 고정 값과 비교하는 인수의 값입니다.

## <a name="return-value"></a>반환 값

이항 함수 개체의 첫 번째 인수 값에 바인딩할 결과로 생성 되는 단항 함수 개체로 *왼쪽*합니다.

## <a name="remarks"></a>설명

이항 함수 개체의 복사본을 저장 하는 템플릿 클래스 *Func* 에서 `op`, 및 사본을 *왼쪽* 에서 `value`합니다. 그리고 **op**( **value**, `right`)를 반환하도록 해당 멤버 함수 `operator()`를 정의합니다.

경우 *Func* 형식의 개체인 `Operation` 및 `c` 상수 이면 [bind1st](../standard-library/functional-functions.md#bind1st) ( `Func`를 `c` ) 해당 하는 `binder1st` 클래스 생성자 `binder1st` \< **작업이**> ( `Func`, `c` )이 고 더 편리 합니다.

## <a name="example"></a>예제

```cpp
// functional_binder1st.cpp
// compile with: /EHsc
#include <vector>
#include <functional>
#include <algorithm>
#include <iostream>

using namespace std;

int main()
{
    vector<int> v1;
    vector<int>::iterator Iter;

    int i;
    for (i = 0; i <= 5; i++)
    {
        v1.push_back(5 * i);
    }

    cout << "The vector v1 = ( ";
    for (Iter = v1.begin(); Iter != v1.end(); Iter++)
        cout << *Iter << " ";
    cout << ")" << endl;

    // Count the number of integers > 10 in the vector
    vector<int>::iterator::difference_type result1;
    result1 = count_if(v1.begin(), v1.end(),
        binder1st<less<int> >(less<int>(), 10));
    cout << "The number of elements in v1 greater than 10 is: "
         << result1 << "." << endl;

    // Compare use of binder2nd fixing 2nd argument:
    // count the number of integers < 10 in the vector
    vector<int>::iterator::difference_type result2;
    result2 = count_if(v1.begin(), v1.end(),
        binder2nd<less<int> >(less<int>(), 10));
    cout << "The number of elements in v1 less than 10 is: "
         << result2 << "." << endl;
}
\* Output:
The vector v1 = ( 0 5 10 15 20 25 )
The number of elements in v1 greater than 10 is: 3.
The number of elements in v1 less than 10 is: 2.
*\
```

## <a name="requirements"></a>요구 사항

**헤더:** \<functional>

**네임스페이스:** std

## <a name="see-also"></a>참고자료

[C++ 표준 라이브러리의 스레드 보안](../standard-library/thread-safety-in-the-cpp-standard-library.md)<br/>
[C++ 표준 라이브러리 참조](../standard-library/cpp-standard-library-reference.md)<br/>
