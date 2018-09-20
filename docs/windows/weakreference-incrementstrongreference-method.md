---
title: 'Weakreference:: Incrementstrongreference 메서드 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::Details::WeakReference::IncrementStrongReference
dev_langs:
- C++
helpviewer_keywords:
- IncrementStrongReference method
ms.assetid: d0232426-a8cb-48b4-99d4-165de2d66cb9
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 345caec13a1e22bc3350f124a8b340282e3a8a42
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46438810"
---
# <a name="weakreferenceincrementstrongreference-method"></a>WeakReference::IncrementStrongReference 메서드

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

## <a name="syntax"></a>구문

```cpp
ULONG IncrementStrongReference();
```

## <a name="return-value"></a>반환 값

증가 된 강력한 참조 수입니다.

## <a name="remarks"></a>설명

현재 강력한 참조 횟수를 증가 시킵니다 **WeakReference** 개체입니다.

## <a name="requirements"></a>요구 사항

**헤더:** implements.h

**Namespace:** Microsoft::WRL::Details

## <a name="see-also"></a>참고 항목

[WeakReference 클래스](../windows/weakreference-class1.md)<br/>
[Microsoft::WRL::Details 네임스페이스](../windows/microsoft-wrl-details-namespace.md)