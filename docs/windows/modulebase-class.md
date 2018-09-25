---
title: ModuleBase 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 09/21/2018
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::Details::ModuleBase
- implements/Microsoft::WRL::Details::ModuleBase::DecrementObjectCount
- implements/Microsoft::WRL::Details::ModuleBase::IncrementObjectCount
- implements/Microsoft::WRL::Details::ModuleBase::ModuleBase
- implements/Microsoft::WRL::Details::ModuleBase::~ModuleBase
dev_langs:
- C++
helpviewer_keywords:
- ModuleBase class
- Microsoft::WRL::Details::ModuleBase::DecrementObjectCount method
- Microsoft::WRL::Details::ModuleBase::IncrementObjectCount method
- Microsoft::WRL::Details::ModuleBase::ModuleBase, constructor
- Microsoft::WRL::Details::ModuleBase::~ModuleBase, destructor
ms.assetid: edce7591-6893-46f7-94a7-382827775548
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: a87b5d617663e87e8c69596e6b1eedca61996b80
ms.sourcegitcommit: edb46b0239a0e616af4ec58906e12338c3e8d2c6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47169556"
---
# <a name="modulebase-class"></a>ModuleBase 클래스

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

## <a name="syntax"></a>구문

```cpp
class ModuleBase;
```

## <a name="remarks"></a>설명

기본 클래스를 나타냅니다 합니다 [모듈](../windows/module-class.md) 클래스입니다.

## <a name="members"></a>멤버

### <a name="public-constructors"></a>Public 생성자

이름                                         | 설명
-------------------------------------------- | ---------------------------------------------------------
[Modulebase:: Modulebase](#modulebase)        | `Module` 클래스의 인스턴스를 초기화합니다.
[ModuleBase:: ~ ModuleBase](#tilde-modulebase) | 현재 인스턴스를 초기화 해제는 `Module` 클래스입니다.

### <a name="public-methods"></a>Public 메서드

이름                                                      | 설명
--------------------------------------------------------- | -------------------------------------------------------------------------
[Modulebase:: Decrementobjectcount](#decrementobjectcount) | 구현 될 때, 개체 수가 감소 모듈에서 추적 합니다.
[Modulebase:: Incrementobjectcount](#incrementobjectcount) | 구현 시 모듈에 의해 추적 되는 개체의 수를 증가 시킵니다.

## <a name="inheritance-hierarchy"></a>상속 계층

`ModuleBase`

## <a name="requirements"></a>요구 사항

**헤더:** implements.h

**Namespace:** Microsoft::WRL::Details

## <a name="tilde-modulebase"></a>ModuleBase:: ~ ModuleBase

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

```cpp
virtual ~ModuleBase();
```

### <a name="remarks"></a>설명

현재 인스턴스를 초기화 해제는 `ModuleBase` 클래스입니다.

## <a name="decrementobjectcount"></a>Modulebase:: Decrementobjectcount

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

```cpp
virtual long DecrementObjectCount() = 0;
```

### <a name="return-value"></a>반환 값

감소 작업 전 수입니다.

### <a name="remarks"></a>설명

구현 될 때, 개체 수가 감소 모듈에서 추적 합니다.

## <a name="incrementobjectcount"></a>Modulebase:: Incrementobjectcount

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

```cpp
virtual long IncrementObjectCount() = 0;
```

### <a name="return-value"></a>반환 값

증가 연산 전 수입니다.

### <a name="remarks"></a>설명

구현 시 모듈에 의해 추적 되는 개체의 수를 증가 시킵니다.

## <a name="modulebase"></a>Modulebase:: Modulebase

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

```cpp
ModuleBase();
```

### <a name="remarks"></a>설명

`Module` 클래스의 인스턴스를 초기화합니다.
