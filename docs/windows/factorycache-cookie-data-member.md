---
title: 'Factorycache:: Cookie 데이터 멤버 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::Details::FactoryCache::cookie
dev_langs:
- C++
helpviewer_keywords:
- cookie data member
ms.assetid: b1bc79af-a896-4e3b-8afa-64733022eddf
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 6dba6e5d7fd478d198e48e9d8517d34e13b43484
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42613668"
---
# <a name="factorycachecookie-data-member"></a>FactoryCache::cookie 데이터 멤버

Windows Runtime c + + 템플릿 라이브러리 인프라를 지원 하며 코드에서 직접 사용할 수 없습니다.

## <a name="syntax"></a>구문

```cpp
union {
   WINRT_REGISTRATION_COOKIE winrt;
   DWORD com;
} cookie;
```

## <a name="remarks"></a>설명

등록된 된 Windows 런타임 또는 COM 클래스 개체를 식별 하 고 개체 등록을 취소 하려면 나중에 사용 되는 값을 포함 합니다.

## <a name="requirements"></a>요구 사항

**헤더:** module.h

**Namespace:** Microsoft::WRL::Details

## <a name="see-also"></a>참고 항목

[FactoryCache 구조체](../windows/factorycache-structure.md)  
[Microsoft::WRL::Details 네임스페이스](../windows/microsoft-wrl-details-namespace.md)