---
title: ArgTraitsHelper 구조체 | Microsoft Docs
ms.custom: ''
ms.date: 09/21/2018
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- event/Microsoft::WRL::Details::ArgTraitsHelper
- event/Microsoft::WRL::Details::ArgTraitsHelper::args
dev_langs:
- C++
helpviewer_keywords:
- Microsoft::WRL::Details::ArgTraitsHelper structure
- Microsoft::WRL::Details::ArgTraitsHelper::args constant
ms.assetid: e3f798da-0aef-4a57-95d3-d38c34c47d72
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: b608f5da893019d7700891968dcdc06489c563ea
ms.sourcegitcommit: 1d9bd38cacbc783fccd3884b7b92062161c91c84
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/03/2018
ms.locfileid: "48234231"
---
# <a name="argtraitshelper-structure"></a>ArgTraitsHelper 구조체

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

## <a name="syntax"></a>구문

```cpp
template<typename TDelegateInterface>
struct ArgTraitsHelper;
```

### <a name="parameters"></a>매개 변수

*TDelegateInterface*<br/>
대리자 인터페이스입니다.

## <a name="remarks"></a>설명

대리자 인수의 공통 된 특징을 정의할 수 있습니다.

## <a name="members"></a>멤버

### <a name="public-typedefs"></a>공용 Typedefs

이름         | 설명
------------ | ------------------------------------------------------
`methodType` | `decltype(&TDelegateInterface::Invoke)`의 동의어입니다.
`Traits`     | `ArgTraits<methodType>`의 동의어입니다.

### <a name="public-constants"></a>공용 상수

이름                           | 설명
------------------------------ | ---------------------------------------------------------------------------------------------------------------------
[Argtraitshelper:: Args](#args) | 데 도움이 됩니다 [argtraits:: Args](#args) 매개 변수 개수를 유지는 `Invoke` 대리자 인터페이스의 메서드입니다.

## <a name="inheritance-hierarchy"></a>상속 계층

`ArgTraitsHelper`

## <a name="requirements"></a>요구 사항

**헤더:** event.h

**Namespace:** Microsoft::WRL::Details

## <a name="args"></a>Argtraitshelper:: Args

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

```cpp
static const int args = Traits::args;
```

### <a name="remarks"></a>설명

데 도움이 됩니다 `ArgTraitsHelper::args` 매개 변수 개수를 유지는 `Invoke` 대리자 인터페이스의 메서드입니다.
