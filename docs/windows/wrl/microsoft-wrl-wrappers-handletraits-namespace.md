---
title: Microsoft::WRL::Wrappers::HandleTraits 네임스페이스
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits
helpviewer_keywords:
- HandleTraits namespace
ms.assetid: 2fb5c6d1-bfc2-4e09-91eb-31705064ffb3
ms.openlocfilehash: 55e1dfea2d4075a5a37b9654a70e9ce74383ea53
ms.sourcegitcommit: 360b55e89e5954f494e52b1cf989fbaceda06f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54336598"
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
|[CriticalSectionTraits 구조체](criticalsectiontraits-structure.md)|전문적으로 다루는 `CriticalSection` 개체는 잘못 된 중요 한 섹션 또는 중요 섹션을 해제 하는 함수를 지원 합니다.|
|[EventTraits 구조체](eventtraits-structure.md)|특성의 정의 `Event` 클래스 핸들입니다.|
|[FileHandleTraits 구조체](filehandletraits-structure.md)|파일 핸들의 특성을 정의합니다.|
|[HANDLENullTraits 구조체](handlenulltraits-structure.md)|초기화 되지 않은 핸들을의 일반적인 특성을 정의합니다.|
|[HANDLETraits 구조체](handletraits-structure.md)|핸들의 공통 된 특징을 정의합니다.|
|[MutexTraits 구조체](mutextraits-structure.md)|일반적인 특성을 정의 합니다 [뮤텍스](mutex-class.md) 클래스입니다.|
|[SemaphoreTraits 구조체](semaphoretraits-structure.md)|세마포 개체의 공통 된 특징을 정의합니다.|
|[SRWLockExclusiveTraits 구조체](srwlockexclusivetraits-structure.md)|일반적인 특징을 설명 합니다 `SRWLock` 배타적 잠금 모드의 클래스입니다.|
|[SRWLockSharedTraits 구조체](srwlocksharedtraits-structure.md)|일반적인 특징을 설명 합니다 `SRWLock` 공유 잠금 모드의 클래스입니다.|

## <a name="requirements"></a>요구 사항

**헤더:** corewrappers.h

**네임스페이스:** Microsoft::WRL::Wrappers

## <a name="see-also"></a>참고 항목

[Microsoft::WRL::Wrappers 네임스페이스](microsoft-wrl-wrappers-namespace.md)