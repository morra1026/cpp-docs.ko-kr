---
title: SemaphoreTraits 구조체 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::SemaphoreTraits
dev_langs:
- C++
helpviewer_keywords:
- SemaphoreTraits structure
ms.assetid: eddb8576-d063-409b-9201-cc87ca5d111e
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 5919b84a8b7b0b24588958198da89271d2a20119
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42601822"
---
# <a name="semaphoretraits-structure"></a>SemaphoreTraits 구조체

일반적인 특성 정의 **세마포** 개체입니다.

## <a name="syntax"></a>구문

```cpp
struct SemaphoreTraits : HANDLENullTraits;
```

## <a name="members"></a>멤버

### <a name="public-methods"></a>Public 메서드

|이름|설명|
|----------|-----------------|
|[SemaphoreTraits::Unlock 메서드](../windows/semaphoretraits-unlock-method.md)|공유 리소스의 릴리스 컨트롤입니다.|

## <a name="inheritance-hierarchy"></a>상속 계층

`HANDLENullTraits`

`SemaphoreTraits`

## <a name="requirements"></a>요구 사항

**헤더:** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers::HandleTraits

## <a name="see-also"></a>참고 항목

[Microsoft::WRL::Wrappers::HandleTraits 네임스페이스](../windows/microsoft-wrl-wrappers-handletraits-namespace.md)