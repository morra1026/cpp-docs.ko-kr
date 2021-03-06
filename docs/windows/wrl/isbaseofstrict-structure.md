---
title: IsBaseOfStrict 구조체
ms.date: 10/03/2018
ms.topic: reference
f1_keywords:
- internal/Microsoft::WRL::Details::IsBaseOfStrict
- internal/Microsoft::WRL::Details::IsBaseOfStrict::value
helpviewer_keywords:
- Microsoft::WRL::Details::IsBaseOfStrict structure
- Microsoft::WRL::Details::IsBaseOfStrict::value constant
ms.assetid: 6fed7366-c8d4-4991-b4fb-43ed93f8e1bf
ms.openlocfilehash: 85aeb71ceaa162cc6366836dd286f2f9983d34e2
ms.sourcegitcommit: 360b55e89e5954f494e52b1cf989fbaceda06f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54336817"
---
# <a name="isbaseofstrict-structure"></a>IsBaseOfStrict 구조체

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

## <a name="syntax"></a>구문

```cpp
template <typename Base, typename Derived>
struct IsBaseOfStrict;

template <typename Base>
struct IsBaseOfStrict<Base, Base>;
```

### <a name="parameters"></a>매개 변수

*Base*<br/>
기본 형식입니다.

*파생 된*<br/>
파생된 형식입니다.

## <a name="remarks"></a>설명

형식 하나가 다른 형식의 기본 형식인지 테스트합니다.

첫 번째 템플릿 형식을 생성 하는 기본 형식에서 파생 됩니다 있는지 여부를 테스트 **true** 하거나 **false**합니다. 두 번째 템플릿은 파생 된 형식 자체에서 항상 생성 하는 여부를 테스트 **false**합니다.

## <a name="members"></a>멤버

### <a name="public-constants"></a>공용 상수

이름                            | 설명
------------------------------- | --------------------------------------------------
[IsBaseOfStrict::value](#value) | 한 형식이 다른 형식의 기본 인지 여부를 나타냅니다.

## <a name="inheritance-hierarchy"></a>상속 계층

`IsBaseOfStrict`

## <a name="requirements"></a>요구 사항

**헤더:** internal.h

**네임스페이스:** Microsoft::WRL::Details

## <a name="value"></a>IsBaseOfStrict::value

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

```cpp
static const bool value = __is_base_of(Base, Derived);
```

### <a name="remarks"></a>설명

한 형식이 다른 형식의 기본 인지 여부를 나타냅니다.

`value` 됩니다 **true** 경우 형식 `Base` 형식의 기본 클래스인 `Derived`, 그렇지 않으면 **false**합니다.
