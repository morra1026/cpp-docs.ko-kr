---
title: Concurrency 네임 스페이스 연산자 (AMP) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.topic: reference
dev_langs:
- C++
ms.assetid: 77f1ae17-1eb2-480d-8fe5-66d4c24bb91e
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: d5844afa476510e4b4984ae69c75193fdf048ddd
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46382364"
---
# <a name="concurrency-namespace-operators-amp"></a>Concurrency 네임 스페이스 연산자 (AMP)

||||
|-|-|-|
|[operator!=](#operator_neq)|[operator%](#operator_mod)|[operator*](#operator_star)|
|[operator+](#operator_add)|[operator-](#operator-)|[operator/](#operator_div)|
|[operator==](#operator_eq_eq)|

##  <a name="operator_eq_eq"></a>  operator==

지정 된 인수를 같은지 여부를 결정 합니다.

```
template <
    int _Rank,
    template <int> class _Tuple_type
>
bool operator== (
    const _Tuple_type<_Rank>& _Lhs,
    const _Tuple_type<_Rank>& _Rhs) restrict(amp);
```

### <a name="parameters"></a>매개 변수

*_Rank*<br/>
튜플 인수의 순위입니다.

*_Lhs*<br/>
비교할 튜플 중 하나입니다.

*_Rhs*<br/>
비교할 튜플 중 하나입니다.

### <a name="return-value"></a>반환 값

`true` 튜플을 같으면 그렇지 않으면 `false`합니다.

##  <a name="operator_neq"></a>  operator!=

지정 된 인수를가 같은지 여부를 결정 합니다.

```
template <
    int _Rank,
    template <int> class _Tuple_type
>
bool operator!= (
    const _Tuple_type<_Rank>& _Lhs,
    const _Tuple_type<_Rank>& _Rhs) restrict(amp);
```

### <a name="parameters"></a>매개 변수

*_Rank*<br/>
튜플 인수의 순위입니다.

*_Lhs*<br/>
비교할 튜플 중 하나입니다.

*_Rhs*<br/>
비교할 튜플 중 하나입니다.

### <a name="return-value"></a>반환 값

`true` 튜플이 서로 다르면; 그렇지 않으면 `false`합니다.

##  <a name="operator_add"></a>  operator+

지정한 인수의 구성 요소별 합을 계산합니다.

```
template <
    int _Rank,
    template <int> class _Tuple_type
>
class _Tuple_type> _Tuple_type<_Rank>   operator+(
    const _Tuple_type<_Rank>& _Lhs,
    const _Tuple_type<_Rank>& _Rhs) restrict(amp,cpu);

template <
    int _Rank,
    template <int> class _Tuple_type
>
class _Tuple_type> _Tuple_type<_Rank>   operator+(
    const _Tuple_type<_Rank>& _Lhs,
    typename _Tuple_type<_Rank>::value_type _Rhs) restrict(amp,cpu);

template <
    int _Rank,
    template <int> class _Tuple_type
>
class _Tuple_type> _Tuple_type<_Rank>   operator+(
    typename _Tuple_type<_Rank>::value_type _Lhs,
    const _Tuple_type<_Rank>& _Rhs) restrict(amp,cpu);
```

### <a name="parameters"></a>매개 변수

*_Rank*<br/>
튜플 인수의 순위입니다.

*_Lhs*<br/>
추가할 인수 중 하나입니다.

*_Rhs*<br/>
추가할 인수 중 하나입니다.

### <a name="return-value"></a>반환 값

지정한 인수의 구성 요소별 합입니다.

##  <a name="operator-"></a>  operator-

지정된 된 인수 사이의 구성 요소별 차이 계산합니다.

```
template <
    int _Rank,
    template <int> class _Tuple_type
>
_Tuple_type<_Rank>   operator-(
    const _Tuple_type<_Rank>& _Lhs,
    const _Tuple_type<_Rank>& _Rhs) restrict(amp,cpu);

template <
    int _Rank,
    template <int> class _Tuple_type
>
_Tuple_type<_Rank>   operator-(
    const _Tuple_type<_Rank>& _Lhs,
    typename _Tuple_type<_Rank>::value_type _Rhs) restrict(amp,cpu);

template <
    int _Rank,
    template <int> class _Tuple_type
>
_Tuple_type<_Rank>   operator-(
    typename _Tuple_type<_Rank>::value_type _Lhs,
    const _Tuple_type<_Rank>& _Rhs) restrict(amp,cpu);
```

### <a name="parameters"></a>매개 변수

*_Rank*<br/>
튜플 인수의 순위입니다.

*_Lhs*<br/>
뺄 인수입니다.

*_Rhs*<br/>
뺄 인수입니다.

### <a name="return-value"></a>반환 값

지정된 된 인수 사이의 구성 요소별 차이입니다.

##  <a name="operator_star"></a>  operator*

지정한 인수의 구성 요소별 곱을 계산합니다.

```
template <
    int _Rank,
    template <int> class _Tuple_type
>
_Tuple_type<_Rank>   operator*(
    const _Tuple_type<_Rank>& _Lhs,
    typename _Tuple_type<_Rank>::value_type _Rhs) restrict(amp,cpu);

template <
    int _Rank,
    template <int> class _Tuple_type
>
_Tuple_type<_Rank>   operator*(
    typename _Tuple_type<_Rank>::value_type _Lhs,
    const _Tuple_type<_Rank>& _Rhs) restrict(amp, cpu);
```

### <a name="parameters"></a>매개 변수

*_Rank*<br/>
튜플 인수의 순위입니다.

*_Lhs*<br/>
곱할 튜플 중 하나입니다.

*_Rhs*<br/>
곱할 튜플 중 하나입니다.

### <a name="return-value"></a>반환 값

지정한 인수의 구성 요소별 곱입니다.

##  <a name="operator_div"></a>  operator/

지정한 인수의 구성 요소별 몫을 계산합니다.

```
template <
    int _Rank,
    template <int> class _Tuple_type
>
_Tuple_type<_Rank>   operator/(
    const _Tuple_type<_Rank>& _Lhs,
    typename _Tuple_type<_Rank>::value_type _Rhs) restrict(amp,cpu);

template <
    int _Rank,
    template <int> class _Tuple_type
>
_Tuple_type<_Rank>   operator/(
    typename _Tuple_type<_Rank>::value_type _Lhs,
    const _Tuple_type<_Rank>& _Rhs) restrict(amp,cpu);
```

### <a name="parameters"></a>매개 변수

*_Rank*<br/>
튜플 인수의 순위입니다.

*_Lhs*<br/>
나누기 작업의 대상 튜플입니다.

*_Rhs*<br/>
나눌에 사용할 튜플입니다.

### <a name="return-value"></a>반환 값

지정한 인수의 구성 요소별 몫입니다.

##  <a name="operator_mod"></a>  operator%

지정 된 두 번째 인수에 의해 지정 된 첫 번째 인수의 모듈러스를 계산 합니다.

```
template <
    int _Rank,
    template <int> class _Tuple_type
>
_Tuple_type<_Rank>   operator%(
    const _Tuple_type<_Rank>& _Lhs,
    typename _Tuple_type<_Rank>::value_type _Rhs) restrict(amp,cpu);

template <
    int _Rank,
    template <int> class _Tuple_type
>
_Tuple_type<_Rank>   operator%(
    typename _Tuple_type<_Rank>::value_type _Lhs,
    const _Tuple_type<_Rank>& _Rhs) restrict(amp,cpu);
```

### <a name="parameters"></a>매개 변수

*_Rank*<br/>
튜플 인수의 순위입니다.

*_Lhs*<br/>
튜플의 나머지를 계산 합니다.

*_Rhs*<br/>
에 사용할 튜플 모듈로.

### <a name="return-value"></a>반환 값

결과 첫 번째 지정 된 인수 모듈러스는 두 번째 지정 된 인수입니다.

## <a name="see-also"></a>참고 항목

[Namespace 동시성 ](concurrency-namespace-cpp-amp.md)
