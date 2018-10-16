---
title: IsSame 구조체 | Microsoft Docs
ms.custom: ''
ms.date: 10/03/2018
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- internal/Microsoft::WRL::Details::IsSame
- internal/Microsoft::WRL::Details::IsSame::value
dev_langs:
- C++
helpviewer_keywords:
- Microsoft::WRL::Details::IsSame structure
- Microsoft::WRL::Details::IsSame::value constant
ms.assetid: 1eddbc3f-3cc5-434f-8495-e4477e1f868e
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 2af59860016835f8e8dfddc9d0a77204ff866bd3
ms.sourcegitcommit: 8480f16893f09911f08a58caf684405404f7ac8e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49161855"
---
# <a name="issame-structure"></a>IsSame 구조체

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

## <a name="syntax"></a>구문

```cpp
template <typename T1, typename T2>
struct IsSame;

template <typename T1>
struct IsSame<T1, T1>;
```

### <a name="parameters"></a>매개 변수

*T1*<br/>
형식입니다.

*T2*<br/>
다른 형식입니다.

## <a name="remarks"></a>설명

형식이 지정 된 것과 같습니다 다른 테스트 형식을 지정 합니다.

## <a name="members"></a>멤버

### <a name="public-constants"></a>공용 상수

이름                    | 설명
----------------------- | --------------------------------------------------
[Issame:: Value](#value) | 한 형식이 다른 동일한 인지 여부를 나타냅니다.

## <a name="inheritance-hierarchy"></a>상속 계층

`IsSame`

## <a name="requirements"></a>요구 사항

**헤더:** internal.h

**Namespace:** Microsoft::WRL::Details

## <a name="value"></a>Issame:: Value

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

```cpp
template <typename T1, typename T2>
struct IsSame
{
    static const bool value = false;
};

template <typename T1>
struct IsSame<T1, T1>
{
    static const bool value = true;
};
```

### <a name="remarks"></a>설명

한 형식이 다른 동일한 인지 여부를 나타냅니다.

`value` 됩니다 **true** 같으면 템플릿 매개 변수, 및 **false** 템플릿 매개 변수는 서로 다른 경우.
