---
title: 'Eventtargetarray:: Begin 메서드 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- event/Microsoft::WRL::Details::EventTargetArray::Begin
dev_langs:
- C++
helpviewer_keywords:
- Begin method
ms.assetid: 1cc7fdfd-a2c4-4b28-93cf-1c82842294ba
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: b818595d8ad32295dbce1498161898b215e1885f
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46433775"
---
# <a name="eventtargetarraybegin-method"></a>EventTargetArray::Begin 메서드

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

## <a name="syntax"></a>구문

```cpp
ComPtr<IUnknown>* Begin();
```

## <a name="return-value"></a>반환 값

이벤트 처리기의 내부 배열에서 첫 번째 요소의 주소입니다.

## <a name="remarks"></a>설명

이벤트 처리기의 내부 배열에서 첫 번째 요소의 주소를 가져옵니다.

## <a name="requirements"></a>요구 사항

**헤더:** event.h

**Namespace:** Microsoft::WRL::Details

## <a name="see-also"></a>참고 항목

[EventTargetArray 클래스](../windows/eventtargetarray-class.md)<br/>
[Microsoft::WRL::Details 네임스페이스](../windows/microsoft-wrl-details-namespace.md)