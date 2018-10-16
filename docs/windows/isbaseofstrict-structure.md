---
title: IsBaseOfStrict 구조체 | Microsoft Docs
ms.custom: ''
ms.date: 10/03/2018
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- internal/Microsoft::WRL::Details::IsBaseOfStrict
- internal/Microsoft::WRL::Details::IsBaseOfStrict::value
dev_langs:
- C++
helpviewer_keywords:
- Microsoft::WRL::Details::IsBaseOfStrict structure
- Microsoft::WRL::Details::IsBaseOfStrict::value constant
ms.assetid: 6fed7366-c8d4-4991-b4fb-43ed93f8e1bf
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 90ceaf20a5d601fc2904b7ce8610b4a3906e30ac
ms.sourcegitcommit: 8480f16893f09911f08a58caf684405404f7ac8e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49161205"
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

*자료*<br/>
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
[Isbaseofstrict:: Value](#value) | 한 형식이 다른 형식의 기본 인지 여부를 나타냅니다.

## <a name="inheritance-hierarchy"></a>상속 계층

`IsBaseOfStrict`

## <a name="requirements"></a>요구 사항

**헤더:** internal.h

**Namespace:** Microsoft::WRL::Details

## <a name="value"></a>Isbaseofstrict:: Value

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

```cpp
static const bool value = __is_base_of(Base, Derived);
```

### <a name="remarks"></a>설명

한 형식이 다른 형식의 기본 인지 여부를 나타냅니다.

`value` 됩니다 **true** 경우 형식 `Base` 형식의 기본 클래스인 `Derived`, 그렇지 않으면 **false**합니다.
