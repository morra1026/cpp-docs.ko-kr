---
title: 'Chaininterfaces:: Casttounknown 메서드 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::ChainInterfaces::CastToUnknown
dev_langs:
- C++
helpviewer_keywords:
- CastToUnknown method
ms.assetid: a6a58555-e5b0-4773-aba0-959d9d362c6b
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 96e7428e2263beb57eb73e024815000d61e75d5f
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42612559"
---
# <a name="chaininterfacescasttounknown-method"></a>ChainInterfaces::CastToUnknown 메서드

정의한 형식의 인터페이스 포인터를 캐스팅 합니다 *I0* 포인터에 대 한 템플릿 매개 변수 `IUnknown`합니다.

## <a name="syntax"></a>구문

```cpp
__forceinline IUnknown* CastToUnknown();
```

## <a name="return-value"></a>반환 값

에 대 한 포인터 `IUnknown`합니다.

## <a name="requirements"></a>요구 사항

**헤더:** implements.h

**네임스페이스:** Microsoft::WRL

## <a name="see-also"></a>참고 항목

[ChainInterfaces 구조체](../windows/chaininterfaces-structure.md)