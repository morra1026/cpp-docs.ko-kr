---
title: is_assignable 클래스 | Microsoft 문서
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
f1_keywords:
- type_traits/std::is_assignable
dev_langs:
- C++
helpviewer_keywords:
- is_assignable
ms.assetid: 53444287-c8be-4ad2-9487-a85c066a4f84
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 339b3cdb2e2470fea976ef8257e6a84f089d3dd9
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45712558"
---
# <a name="isassignable-class"></a>is_assignable 클래스

`From` 형식의 값을 `To` 형식에 할당할 수 있는지 여부를 테스트합니다.

## <a name="syntax"></a>구문

```cpp
template <class To, class From>
struct is_assignable;
```

### <a name="parameters"></a>매개 변수

*대상*<br/>
할당을 받는 개체의 형식입니다.

*From*<br/>
값을 제공하는 개체의 형식입니다.

## <a name="remarks"></a>설명

평가되지 않은 `declval<To>() = declval<From>()` 식은 올바른 형식이어야 합니다. 둘 다 `From` 하 고 `To` 완전 한 형식 이어야 합니다 **void**, 또는 범위를 알 수 없는 배열입니다.

## <a name="requirements"></a>요구 사항

**헤더:** \<type_traits>

**네임스페이스:** std

## <a name="see-also"></a>참고자료

[<type_traits>](../standard-library/type-traits.md)<br/>
