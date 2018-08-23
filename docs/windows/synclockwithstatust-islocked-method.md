---
title: 'Synclockwithstatust:: Islocked 메서드 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::Details::SyncLockWithStatusT::IsLocked
dev_langs:
- C++
helpviewer_keywords:
- IsLocked method
ms.assetid: e1b75b7b-c145-471a-aa5d-71abf31f5990
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: d70a2c316f9e7994292f3dc29cef5bce993778ad
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42595065"
---
# <a name="synclockwithstatustislocked-method"></a>SyncLockWithStatusT::IsLocked 메서드

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

## <a name="syntax"></a>구문

```cpp
bool IsLocked() const;
```

## <a name="remarks"></a>설명

나타냅니다 여부 현재 **SyncLockWithStatusT** 리소스를 소유 하는 개체입니다. 즉, **SyncLockWithStatusT** 개체가 *잠겨*합니다.

## <a name="return-value"></a>반환 값

**true** 경우는 **SyncLockWithStatusT** 개체가 고, 그렇지 않으면 잠긴 **false**합니다.

## <a name="requirements"></a>요구 사항

**헤더:** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers::Details

## <a name="see-also"></a>참고 항목

[SyncLockWithStatusT 클래스](../windows/synclockwithstatust-class.md)