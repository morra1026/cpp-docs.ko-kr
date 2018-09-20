---
title: 'Srwlock:: Trylockexclusive 메서드 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::SRWLock::TryLockExclusive
dev_langs:
- C++
helpviewer_keywords:
- TryLockExclusive method
ms.assetid: 661e8b19-3058-4511-8742-c9fbb90412c7
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: d0deec4790d185a5c6b7a7bdcbd670b056fc6f03
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46424107"
---
# <a name="srwlocktrylockexclusive-method"></a>SRWLock::TryLockExclusive 메서드

획득 하 려는 **SRWLock** 개체의 현재 또는 지정 된 단독 모드 **SRWLock** 개체입니다. 호출이 성공 하면 호출 스레드는 잠금 소유권을 받습니다.

## <a name="syntax"></a>구문

```cpp
SyncLockExclusive TryLockExclusive();

static SyncLockExclusive TryLockExclusive(
   _In_ SRWLOCK* lock
);
```

### <a name="parameters"></a>매개 변수

*lock*<br/>
에 대 한 포인터를 **SRWLock** 개체입니다.

## <a name="return-value"></a>반환 값

성공한 경우는 **SRWLock** 개체 단독 모드 및 호출 스레드는 잠금 소유권을 받습니다. 그렇지 않은 경우는 **SRWLock** 개체 상태가 올바르지 않습니다.

## <a name="requirements"></a>요구 사항

**헤더:** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers

## <a name="see-also"></a>참고 항목

[SRWLock 클래스](../windows/srwlock-class.md)