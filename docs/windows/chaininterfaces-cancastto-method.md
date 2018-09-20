---
title: 'Chaininterfaces:: Cancastto 메서드 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::ChainInterfaces::CanCastTo
dev_langs:
- C++
helpviewer_keywords:
- CanCastTo method
ms.assetid: 8be44875-53ed-494b-91a0-0f8e399685bb
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 752c3598a38117506154b0a2b7d7d3e578bf3c3e
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46417646"
---
# <a name="chaininterfacescancastto-method"></a>ChainInterfaces::CanCastTo 메서드

각 기본이 아닌 템플릿 매개 변수를 정의한 특수화에 지정 된 인터페이스 ID 캐스팅 될 수 있는지 여부를 나타냅니다.

## <a name="syntax"></a>구문

```cpp
__forceinline bool CanCastTo(
   REFIID riid,
   _Deref_out_ void **ppv
);
```

### <a name="parameters"></a>매개 변수

*riid*<br/>
인터페이스 ID입니다.

*ppv*<br/>
성공적으로 캐스팅 된 마지막 인터페이스 ID에 대 한 포인터입니다.

## <a name="return-value"></a>반환 값

**true 이면** 모든 캐스트 작업이 성공 하면이 고, 그렇지 **false**합니다.

## <a name="requirements"></a>요구 사항

**헤더:** implements.h

**네임스페이스:** Microsoft::WRL

## <a name="see-also"></a>참고 항목

[ChainInterfaces 구조체](../windows/chaininterfaces-structure.md)