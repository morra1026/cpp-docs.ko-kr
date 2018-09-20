---
title: VerifyInheritanceHelper 구조체 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::Details::VerifyInheritanceHelper
dev_langs:
- C++
helpviewer_keywords:
- VerifyInheritanceHelper structure
ms.assetid: 8a48a702-0f71-4807-935b-8311f0a7a8b6
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: ddd358c3eb20439f87de8614d80af01537ae31e6
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46396575"
---
# <a name="verifyinheritancehelper-structure"></a>VerifyInheritanceHelper 구조체

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

## <a name="syntax"></a>구문

```cpp
template <
   typename I,
   typename Base
>
struct VerifyInheritanceHelper;
template <
   typename I
>
struct VerifyInheritanceHelper<I, Nil>;
```

### <a name="parameters"></a>매개 변수

*I*<br/>
형식입니다.

*자료*<br/>
다른 형식입니다.

## <a name="remarks"></a>설명

하나의 인터페이스는 다른 인터페이스에서 파생 됩니다 있는지 테스트 합니다.

## <a name="members"></a>멤버

### <a name="public-methods"></a>Public 메서드

|이름|설명|
|----------|-----------------|
|[VerifyInheritanceHelper::Verify 메서드](../windows/verifyinheritancehelper-verify-method.md)|현재 템플릿 매개 변수로 지정 된 두 가지 인터페이스를 테스트 하 고 하나의 인터페이스는 다른 파생 되었는지 여부를 결정 합니다.|

## <a name="inheritance-hierarchy"></a>상속 계층

`VerifyInheritanceHelper`

## <a name="requirements"></a>요구 사항

**헤더:** implements.h

**Namespace:** Microsoft::WRL::Details

## <a name="see-also"></a>참고 항목

[Microsoft::WRL::Details 네임스페이스](../windows/microsoft-wrl-details-namespace.md)