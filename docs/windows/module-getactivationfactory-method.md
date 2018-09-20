---
title: 'Module:: getactivationfactory 메서드 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::Module::GetActivationFactory
dev_langs:
- C++
helpviewer_keywords:
- GetActivationFactory method
ms.assetid: 59da8844-072e-414b-b89c-1db1cc4fd81d
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 995594ee48e6ca408e88d9ab14968d88b536d309
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46403518"
---
# <a name="modulegetactivationfactory-method"></a>Module::GetActivationFactory 메서드

모듈에 대한 활성화 팩터리를 가져옵니다.

## <a name="syntax"></a>구문

```cpp
WRL_NOTHROW HRESULT GetActivationFactory(
   _In_ HSTRING pActivatibleClassId,
   _Deref_out_ IActivationFactory **ppIFactory,
   wchar_t* serverName = nullptr
);
```

### <a name="parameters"></a>매개 변수

*pActivatibleClassId*<br/>
런타임 클래스의 IID입니다.

*ppIFactory*<br/>
지정된 런타임 클래스에 대한 IActivationFactory입니다.

*서버 이름*<br/>
현재 모듈의 클래스 팩터리 하위 집합 이름입니다. 에 사용 되는 서버 이름을 지정 합니다 [ActivatableClassWithFactoryEx](../windows/activatableclass-macros.md) 매크로 지정 하거나 **nullptr** 기본 서버 이름을 가져올 수 합니다.

## <a name="return-value"></a>반환 값

성공하면 S_OK이고, 그렇지 않으면 GetActivationFactory에서 반환된 HRESULT입니다.

## <a name="requirements"></a>요구 사항

**헤더:** module.h

**네임스페이스:** Microsoft::WRL

## <a name="see-also"></a>참고 항목

[Module 클래스](../windows/module-class.md)<br/>
[ActivatableClass 매크로](../windows/activatableclass-macros.md)