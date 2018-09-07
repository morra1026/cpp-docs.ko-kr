---
title: '&lt;scoped_allocator&gt; 연산자 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- scoped_allocator/std::operator!=
- scoped_allocator/std::operator==
dev_langs:
- C++
ms.assetid: 4dfe0805-cc6e-479f-887f-a1c164f73837
ms.openlocfilehash: 0dda1415ea875b01c943a0a275122458f399f69c
ms.sourcegitcommit: 761c5f7c506915f5a62ef3847714f43e9b815352
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44105882"
---
# <a name="ltscopedallocatorgt-operators"></a>&lt;scoped_allocator&gt; 연산자

|||
|-|-|
|[operator!=](#op_neq)|[operator==](#op_eq_eq)|

## <a name="op_neq"></a>  operator!=

두 `scoped_allocator_adaptor` 개체가 다른지 비교합니다.

```cpp
template <class Outer, class... Inner>
bool operator!=(
    const scoped_allocator_adaptor<Outer, Inner...>& left,
    const scoped_allocator_adaptor<Outer, Inner...>& right) noexcept;
```

### <a name="parameters"></a>매개 변수

*left*<br/>
왼쪽 `scoped_allocator_adaptor` 개체입니다.

*right*<br/>
오른쪽 `scoped_allocator_adaptor` 개체입니다.

### <a name="return-value"></a>반환 값

`!(left == right)`

## <a name="op_eq_eq"></a>  operator==

두 `scoped_allocator_adaptor` 개체가 같은지 테스트합니다.

```cpp
template <class Outer, class... Inner>
bool operator==(
    const scoped_allocator_adaptor<Outer, Inner...>& left,
    const scoped_allocator_adaptor<Outer, Inner...>& right) noexcept;
```

### <a name="parameters"></a>매개 변수

*left*<br/>
왼쪽 `scoped_allocator_adaptor` 개체입니다.

*right*<br/>
오른쪽 `scoped_allocator_adaptor` 개체입니다.

### <a name="return-value"></a>반환 값

`left.outer_allocator() == right.outer_allocator() && left.inner_allocator() == right.inner_allocator()`

## <a name="see-also"></a>참고자료

[<scoped_allocator>](../standard-library/scoped-allocator.md)<br/>
