---
title: 'Module:: unregisterwinrtobject 메서드 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::Module::UnregisterWinRTObject
dev_langs:
- C++
helpviewer_keywords:
- UnregisterWinRTObject method
ms.assetid: 32334aa7-2293-40d2-9a89-4b02e2e31f3c
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 39bb86206aec72d918df482ee1d01214b4fbb03b
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46381753"
---
# <a name="moduleunregisterwinrtobject-method"></a>Module::UnregisterWinRTObject 메서드

다른 응용 프로그램과 연결할 수 있도록 하나 이상의 Windows 런타임 개체를 등록 취소 합니다.

## <a name="syntax"></a>구문

```cpp
virtual HRESULT UnregisterWinRTObject(
   unsigned int,
   _Inout_ WINRT_REGISTRATION_COOKIE* cookie
);
```

### <a name="parameters"></a>매개 변수

*쿠키*<br/>
등록이 해지된 클래스 개체를 식별하는 값에 대한 포인터입니다.

## <a name="requirements"></a>요구 사항

**헤더:** module.h

**네임스페이스:** Microsoft::WRL

## <a name="see-also"></a>참고 항목

[Module 클래스](../windows/module-class.md)