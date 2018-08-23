---
title: Microsoft::WRL::Wrappers::HandleTraits Namespace | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits
dev_langs:
- C++
helpviewer_keywords:
- HandleTraits namespace
ms.assetid: 2fb5c6d1-bfc2-4e09-91eb-31705064ffb3
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 683759c3bf0b2152ee6fadbb638cd2398daecccd
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42586131"
---
# <a name="microsoftwrlwrappershandletraits-namespace"></a>Microsoft::WRL::Wrappers::HandleTraits 네임스페이스

일반적인 핸들 기반 리소스 종류의 특징을 설명 합니다.

## <a name="syntax"></a>구문

```cpp
namespace Microsoft::WRL::Wrappers::HandleTraits;
```

## <a name="members"></a>멤버

### <a name="structures"></a>구조체

|이름|설명|
|----------|-----------------|
|[CriticalSectionTraits 구조체](../windows/criticalsectiontraits-structure.md)|전문적으로 다루는 `CriticalSection` 개체는 잘못 된 중요 한 섹션 또는 중요 섹션을 해제 하는 함수를 지원 합니다.|
|[EventTraits 구조체](../windows/eventtraits-structure.md)|특성의 정의 `Event` 클래스 핸들입니다.|
|[FileHandleTraits 구조체](../windows/filehandletraits-structure.md)|파일 핸들의 특성을 정의합니다.|
|[HANDLENullTraits 구조체](../windows/handlenulltraits-structure.md)|초기화 되지 않은 핸들을의 일반적인 특성을 정의합니다.|
|[HANDLETraits 구조체](../windows/handletraits-structure.md)|핸들의 공통 된 특징을 정의합니다.|
|[MutexTraits 구조체](../windows/mutextraits-structure.md)|일반적인 특성을 정의 합니다 [뮤텍스](../windows/mutex-class1.md) 클래스입니다.|
|[SemaphoreTraits 구조체](../windows/semaphoretraits-structure.md)|세마포 개체의 공통 된 특징을 정의합니다.|
|[SRWLockExclusiveTraits 구조체](../windows/srwlockexclusivetraits-structure.md)|일반적인 특징을 설명 합니다 `SRWLock` 배타적 잠금 모드의 클래스입니다.|
|[SRWLockSharedTraits 구조체](../windows/srwlocksharedtraits-structure.md)|일반적인 특징을 설명 합니다 `SRWLock` 공유 잠금 모드의 클래스입니다.|

## <a name="requirements"></a>요구 사항

**헤더:** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers

## <a name="see-also"></a>참고 항목

[Microsoft::WRL::Wrappers 네임스페이스](../windows/microsoft-wrl-wrappers-namespace.md)