---
title: MutexTraits 구조체
ms.date: 09/27/2018
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::MutexTraits
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::MutexTraits::Unlock
helpviewer_keywords:
- Microsoft::WRL::Wrappers::HandleTraits::MutexTraits structure
- Microsoft::WRL::Wrappers::HandleTraits::MutexTraits::Unlock method
ms.assetid: 6582df80-b9ba-4892-948f-d572a3b23d54
ms.openlocfilehash: 84bfac08a944928ff91a7734cdbaccbe4d351e16
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50650751"
---
# <a name="mutextraits-structure"></a>MutexTraits 구조체

일반적인 특성을 정의 합니다 [뮤텍스](../windows/mutex-class1.md) 클래스입니다.

## <a name="syntax"></a>구문

```cpp
struct MutexTraits : HANDLENullTraits;
```

## <a name="members"></a>멤버

### <a name="public-methods"></a>Public 메서드

이름                           | 설명
------------------------------ | ------------------------------------------------
[Mutextraits:: Unlock](#unlock) | 공유 리소스의 한 독점적인 제어권을 해제합니다.

## <a name="inheritance-hierarchy"></a>상속 계층

`HANDLENullTraits`

`MutexTraits`

## <a name="requirements"></a>요구 사항

**헤더:** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers::HandleTraits

## <a name="unlock"></a>Mutextraits:: Unlock 메서드

공유 리소스의 한 독점적인 제어권을 해제합니다.

```cpp
inline static void Unlock(
   _In_ Type h
);
```

### <a name="parameters"></a>매개 변수

*h*<br/>
뮤텍스 개체에 대 한 핸들입니다.
