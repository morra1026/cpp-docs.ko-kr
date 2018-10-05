---
title: SRWLockExclusiveTraits 구조체 | Microsoft Docs
ms.custom: ''
ms.date: 09/27/2018
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::SRWLockExclusiveTraits
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::SRWLockExclusiveTraits::GetInvalidValue
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::SRWLockExclusiveTraits::Unlock
dev_langs:
- C++
helpviewer_keywords:
- Microsoft::WRL::Wrappers::HandleTraits::SRWLockExclusiveTraits structure
- Microsoft::WRL::Wrappers::HandleTraits::SRWLockExclusiveTraits::GetInvalidValue method
- Microsoft::WRL::Wrappers::HandleTraits::SRWLockExclusiveTraits::Unlock method
ms.assetid: 38a996ef-c2d7-4886-b413-a426ecee8f05
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 7737c802634b618b9ea363c231a44d9381ad30ae
ms.sourcegitcommit: 1d9bd38cacbc783fccd3884b7b92062161c91c84
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/03/2018
ms.locfileid: "48235167"
---
# <a name="srwlockexclusivetraits-structure"></a>SRWLockExclusiveTraits 구조체

일반적인 특징을 설명 합니다 `SRWLock` 배타적 잠금 모드의 클래스입니다.

## <a name="syntax"></a>구문

```cpp
struct SRWLockExclusiveTraits;
```

## <a name="members"></a>멤버

### <a name="public-typedefs"></a>공용 Typedefs

이름   | 설명
------ | --------------------------------------------------------------------------
`Type` | 동의어에 대 한 포인터를 [SRWLOCK](../windows/srwlock-class.md) 클래스입니다.

### <a name="public-methods"></a>Public 메서드

이름                                                        | 설명
----------------------------------------------------------- | --------------------------------------------------------------------
[Srwlockexclusivetraits:: Getinvalidvalue](#getinvalidvalue) | 검색을 `SRWLockExclusiveTraits` 항상 유효 하지 않은 개체입니다.
[Srwlockexclusivetraits:: Unlock](#unlock)                   | 지정 된 한 독점적인 제어권을 해제 `SRWLock` 개체입니다.

## <a name="inheritance-hierarchy"></a>상속 계층

`SRWLockExclusiveTraits`

## <a name="requirements"></a>요구 사항

**헤더:** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers::HandleTraits

## <a name="getinvalidvalue"></a>Srwlockexclusivetraits:: Getinvalidvalue

검색을 `SRWLockExclusiveTraits` 항상 유효 하지 않은 개체입니다.

```cpp
inline static Type GetInvalidValue();
```

### <a name="return-value"></a>반환 값

빈 `SRWLockExclusiveTraits` 개체입니다.

## <a name="unlock"></a>Srwlockexclusivetraits:: Unlock

지정 된 한 독점적인 제어권을 해제 `SRWLock` 개체입니다.

```cpp
inline static void Unlock(
   _In_ Type srwlock
);
```

### <a name="parameters"></a>매개 변수

*srwlock*<br/>
에 대 한 핸들을 `SRWLock` 개체입니다.
