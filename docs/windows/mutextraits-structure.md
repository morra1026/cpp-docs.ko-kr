---
title: MutexTraits 구조체 | Microsoft Docs
ms.custom: ''
ms.date: 09/27/2018
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::MutexTraits
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::MutexTraits::Unlock
dev_langs:
- C++
helpviewer_keywords:
- Microsoft::WRL::Wrappers::HandleTraits::MutexTraits structure
- Microsoft::WRL::Wrappers::HandleTraits::MutexTraits::Unlock method
ms.assetid: 6582df80-b9ba-4892-948f-d572a3b23d54
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 15ed7d9dc3a1b97e05712e003fa61f662901fc18
ms.sourcegitcommit: 1d9bd38cacbc783fccd3884b7b92062161c91c84
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/03/2018
ms.locfileid: "48234993"
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
