---
title: HandleT 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 10/03/2018
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::HandleT
- corewrappers/Microsoft::WRL::Wrappers::HandleT::Attach
- corewrappers/Microsoft::WRL::Wrappers::HandleT::Close
- corewrappers/Microsoft::WRL::Wrappers::HandleT::Detach
- corewrappers/Microsoft::WRL::Wrappers::HandleT::Get
- corewrappers/Microsoft::WRL::Wrappers::HandleT::handle_
- corewrappers/Microsoft::WRL::Wrappers::HandleT::HandleT
- corewrappers/Microsoft::WRL::Wrappers::HandleT::InternalClose
- corewrappers/Microsoft::WRL::Wrappers::HandleT::IsValid
- corewrappers/Microsoft::WRL::Wrappers::HandleT::operator=
- corewrappers/Microsoft::WRL::Wrappers::HandleT::~HandleT
dev_langs:
- C++
helpviewer_keywords:
- Microsoft::WRL::Wrappers::HandleT class
- Microsoft::WRL::Wrappers::HandleT::Attach method
- Microsoft::WRL::Wrappers::HandleT::Close method
- Microsoft::WRL::Wrappers::HandleT::Detach method
- Microsoft::WRL::Wrappers::HandleT::Get method
- Microsoft::WRL::Wrappers::HandleT::handle_ data member
- Microsoft::WRL::Wrappers::HandleT::HandleT, constructor
- Microsoft::WRL::Wrappers::HandleT::InternalClose method
- Microsoft::WRL::Wrappers::HandleT::IsValid method
- Microsoft::WRL::Wrappers::HandleT::operator= operator
- Microsoft::WRL::Wrappers::HandleT::~HandleT, destructor
ms.assetid: 3822b32a-a426-4d94-a54d-919d4df60ee2
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: d0f7364ac86aebd0f5a9a1c0f7ec2343b9e162d0
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50081670"
---
# <a name="handlet-class"></a>HandleT 클래스

개체에 대한 핸들을 나타냅니다.

## <a name="syntax"></a>구문

```cpp
template <typename HandleTraits>
class HandleT;
```

### <a name="parameters"></a>매개 변수

*HandleTraits*<br/>
인스턴스를 [HandleTraits](../windows/handletraits-structure.md) 핸들의 공통 된 특징을 정의 하는 구조입니다.

## <a name="members"></a>멤버

### <a name="public-typedefs"></a>공용 Typedefs

이름     | 설명
-------- | -----------------------------
`Traits` | `HandleTraits`의 동의어입니다.

### <a name="public-constructors"></a>Public 생성자

이름                                | 설명
----------------------------------- | --------------------------------------------------
[Handlet:: Handlet](#handlet)        | `HandleT` 클래스의 새 인스턴스를 초기화합니다.
[HandleT:: ~ HandleT](#tilde-handlet) | 인스턴스를 초기화 해제는 `HandleT` 클래스입니다.

### <a name="public-methods"></a>Public 메서드

이름                         | 설명
---------------------------- | ----------------------------------------------------------------------
[Handlet:: Attach](#attach)   | 현재 지정된 된 핸들과 연결 `HandleT` 개체입니다.
[Handlet:: Close](#close)     | 현재 닫습니다 `HandleT` 개체입니다.
[Handlet:: Detach](#detach)   | 현재 연결을 끊습니다 `HandleT` 해당 기본 핸들에서 개체입니다.
[Handlet:: Get](#get)         | 기본 핸들의 값을 가져옵니다.
[Handlet:: Isvalid](#isvalid) | 나타냅니다 여부 현재 `HandleT` 개체 핸들을 나타냅니다.

### <a name="protected-methods"></a>보호된 메서드

이름                                     | 설명
---------------------------------------- | ------------------------------------
[Handlet:: Internalclose](#internalclose) | 현재 닫습니다 `HandleT` 개체입니다.

### <a name="public-operators"></a>Public 연산자

이름                                   | 설명
-------------------------------------- | ----------------------------------------------------------------------------------
[Handlet:: Operator =](#operator-assign) | 지정 된 값을 이동 `HandleT` 개체를 현재 `HandleT` 개체입니다.

### <a name="protected-data-members"></a>보호된 데이터 멤버

이름                        | 설명
--------------------------- | ----------------------------------------------------------------
[Handlet:: Handle_](#handle) | 핸들을 나타내는 포함 된 `HandleT` 개체입니다.

## <a name="inheritance-hierarchy"></a>상속 계층

`HandleT`

## <a name="requirements"></a>요구 사항

**헤더:** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers

## <a name="tilde-handlet"></a>HandleT:: ~ HandleT

인스턴스를 초기화 해제는 `HandleT` 클래스입니다.

```cpp
~HandleT();
```

## <a name="attach"></a>Handlet:: Attach

현재 지정된 된 핸들과 연결 `HandleT` 개체입니다.

```cpp
void Attach(
   typename HandleTraits::Type h
);
```

### <a name="parameters"></a>매개 변수

*h*<br/>
핸들입니다.

## <a name="close"></a>Handlet:: Close

현재 닫습니다 `HandleT` 개체입니다.

```cpp
void Close();
```

### <a name="remarks"></a>설명

현재의 기반이 되는 핸들 `HandleT` 닫혀 및 `HandleT` 잘못 된 상태로 설정 됩니다.

핸들이 제대로 닫히지 않은 경우 호출 스레드에서 예외가 발생합니다.

## <a name="detach"></a>Handlet:: Detach

현재 연결을 끊습니다 `HandleT` 해당 기본 핸들에서 개체입니다.

```cpp
typename HandleTraits::Type Detach();
```

### <a name="return-value"></a>반환 값

기본 핸들입니다.

### <a name="remarks"></a>설명

이 작업이 완료 되 면, 현재 `HandleT` 잘못 된 상태로 설정 됩니다.

## <a name="get"></a>Handlet:: Get

기본 핸들의 값을 가져옵니다.

```cpp
typename HandleTraits::Type Get() const;
```

### <a name="return-value"></a>반환 값

핸들입니다.

## <a name="handle"></a>Handlet:: Handle_

핸들을 나타내는 포함 된 `HandleT` 개체입니다.

```cpp
typename HandleTraits::Type handle_;
```

## <a name="handlet"></a>Handlet:: Handlet

`HandleT` 클래스의 새 인스턴스를 초기화합니다.

```cpp
explicit HandleT(
   typename HandleTraits::Type h =
      HandleTraits::GetInvalidValue()
);

HandleT(
   _Inout_ HandleT&& h
);
```

### <a name="parameters"></a>매개 변수

*h*<br/>
핸들입니다.

### <a name="remarks"></a>설명

첫 번째 생성자는 초기화를 `HandleT` 개체 개체에 대 한 유효한 핸들입니다. 두 번째 생성자를 만듭니다 `HandleT` 매개 변수에서 개체 *h*합니다.

## <a name="internalclose"></a>Handlet:: Internalclose

현재 닫습니다 `HandleT` 개체입니다.

```cpp
virtual bool InternalClose();
```

### <a name="return-value"></a>반환 값

**true** 하는 경우 현재 `HandleT` 이 고, 그렇지 않으면 닫은 **false**합니다.

### <a name="remarks"></a>설명

`InternalClose()`가 `protected`인 경우

## <a name="isvalid"></a>Handlet:: Isvalid

나타냅니다 여부 현재 `HandleT` 개체 핸들을 나타냅니다.

```cpp
bool IsValid() const;
```

### <a name="return-value"></a>반환 값

**true** 경우는 `HandleT` 핸들을 나타내는 고, 그렇지 않으면 **false**합니다.

## <a name="operator-assign"></a>Handlet:: Operator =

지정 된 값을 이동 `HandleT` 개체를 현재 `HandleT` 개체입니다.

```cpp
HandleT& operator=(
   _Inout_ HandleT&& h
);
```

### <a name="parameters"></a>매개 변수

*h*<br/>
핸들에 rvalue 참조입니다.

### <a name="return-value"></a>반환 값

현재에 대 한 참조 `HandleT` 개체입니다.

### <a name="remarks"></a>설명

이 작업을 무효화 합니다 `HandleT` 매개 변수로 지정 된 개체 *h*합니다.
