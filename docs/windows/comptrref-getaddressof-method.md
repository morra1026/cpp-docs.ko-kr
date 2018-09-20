---
title: 'Comptrref:: Getaddressof 메서드 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- client/Microsoft::WRL::Details::ComPtrRef::GetAddressOf
dev_langs:
- C++
helpviewer_keywords:
- GetAddressOf method
ms.assetid: 797df323-a2fa-412b-ab60-32cce3721096
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: a0f35bbe2bdc0d0c8d3500e6b157da542458b1fe
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46421022"
---
# <a name="comptrrefgetaddressof-method"></a>ComPtrRef::GetAddressOf 메서드

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

## <a name="syntax"></a>구문

```cpp
InterfaceType* const * GetAddressOf() const;
```

## <a name="return-value"></a>반환 값

현재이 나타내는 인터페이스에 대 한 포인터 주소의 **ComPtrRef** 개체입니다.

## <a name="remarks"></a>설명

현재이 나타내는 인터페이스에 대 한 포인터의 주소를 검색 **ComPtrRef** 개체입니다.

## <a name="requirements"></a>요구 사항

**헤더:** client.h

**Namespace:** Microsoft::WRL::Details

## <a name="see-also"></a>참고 항목

[ComPtrRef 클래스](../windows/comptrref-class.md)<br/>
[Microsoft::WRL::Details 네임스페이스](../windows/microsoft-wrl-details-namespace.md)