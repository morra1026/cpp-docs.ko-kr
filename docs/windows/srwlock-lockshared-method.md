---
title: 'Srwlock:: Lockshared 메서드 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::SRWLock::LockShared
dev_langs:
- C++
helpviewer_keywords:
- LockShared method
ms.assetid: 9d826a5c-b6a2-4430-ac85-d5753cbca889
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 62667d20e40e04f9202fcb5dfa2f1688b98a3c2d
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46429044"
---
# <a name="srwlocklockshared-method"></a>SRWLock::LockShared 메서드

획득 한 **SRWLock** 공유 모드의 개체입니다.

## <a name="syntax"></a>구문

```cpp
SyncLockShared LockShared();

static SyncLockShared LockShared(
   _In_ SRWLOCK* lock
);
```

### <a name="parameters"></a>매개 변수

*lock*<br/>
에 대 한 포인터를 **SRWLock** 개체입니다.

## <a name="return-value"></a>반환 값

**SRWLock** 공유 모드의 개체입니다.

## <a name="requirements"></a>요구 사항

**헤더:** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers

## <a name="see-also"></a>참고 항목

[SRWLock 클래스](../windows/srwlock-class.md)