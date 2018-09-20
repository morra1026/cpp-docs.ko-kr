---
title: 'Srwlock:: Trylockshared 메서드 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::SRWLock::TryLockShared
dev_langs:
- C++
helpviewer_keywords:
- TryLockShared method
ms.assetid: 10cc198d-39a0-4d18-aa78-706744948668
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 985629f224f199d1b1f095847e64cc67fa5a97f9
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46388469"
---
# <a name="srwlocktrylockshared-method"></a>SRWLock::TryLockShared 메서드

획득 하 려는 **SRWLock** 개체를 현재 또는 지정 된 공유 모드로 **SRWLock** 개체입니다.

## <a name="syntax"></a>구문

```cpp
WRL_NOTHROW SyncLockShared TryLockShared();
WRL_NOTHROW static SyncLockShared TryLockShared(
   _In_ SRWLOCK* lock
);
```

### <a name="parameters"></a>매개 변수

*lock*<br/>
에 대 한 포인터를 **SRWLock** 개체입니다.

## <a name="return-value"></a>반환 값

성공한 경우는 **SRWLock** 개체 공유 모드 및 호출 스레드는 잠금 소유권을 받습니다. 그렇지 않은 경우는 **SRWLock** 개체 상태가 올바르지 않습니다.

## <a name="requirements"></a>요구 사항

**헤더:** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers

## <a name="see-also"></a>참고 항목

[SRWLock 클래스](../windows/srwlock-class.md)