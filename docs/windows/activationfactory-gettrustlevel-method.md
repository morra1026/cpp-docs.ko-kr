---
title: 'Activationfactory:: Gettrustlevel 메서드 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::ActivationFactory::GetTrustLevel
dev_langs:
- C++
helpviewer_keywords:
- GetTrustLevel method
ms.assetid: 31547ae6-d2ab-4039-923c-154d53fb1a8b
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: bfec8bfa6940fd4a702334f0d3068c6d936ea8c1
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42607316"
---
# <a name="activationfactorygettrustlevel-method"></a>ActivationFactory::GetTrustLevel 메서드

개체의 신뢰 수준을 가져옵니다 현재 **ActivationFactory** 인스턴스화합니다.

## <a name="syntax"></a>구문

```cpp
STDMETHOD(
   GetTrustLevel
)(_Out_ TrustLevel* trustLvl);
```

### <a name="parameters"></a>매개 변수

*trustLvl*  
이 작업이 완료 되 면 런타임에서의 신뢰 수준을 클래스는 **ActivationFactory** 인스턴스화합니다.

## <a name="return-value"></a>반환 값

성공 하면 s_ok이 고 어설션 오류가 내보내집니다. 그렇지 않은 경우 및 *trustLvl* 로 설정 된 `FullTrust`합니다.

## <a name="requirements"></a>요구 사항

**헤더:** module.h

**네임스페이스:** Microsoft::WRL

## <a name="see-also"></a>참고 항목

[ActivationFactory 클래스](../windows/activationfactory-class.md)