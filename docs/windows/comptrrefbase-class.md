---
title: ComPtrRefBase 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 09/21/2018
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- client/Microsoft::WRL::Details::ComPtrRefBase
- client/Microsoft::WRL::Details::ComPtrRefBase::operator IInspectable**
- client/Microsoft::WRL::Details::ComPtrRefBase::operator IUnknown**
- client/Microsoft::WRL::Details::ComPtrRefBase::ptr_
dev_langs:
- C++
helpviewer_keywords:
- Microsoft::WRL::Details::ComPtrRefBase class
- Microsoft::WRL::Details::ComPtrRefBase::operator IInspectable** operator
- Microsoft::WRL::Details::ComPtrRefBase::operator IUnknown** operator
- Microsoft::WRL::Details::ComPtrRefBase::ptr_ data member
ms.assetid: 6d344c1a-cc13-4a3f-8a0d-f167ccb9348f
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 02e430184c5fa7418eb02ed6ef2f63951af89a5c
ms.sourcegitcommit: 1d9bd38cacbc783fccd3884b7b92062161c91c84
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/03/2018
ms.locfileid: "48233959"
---
# <a name="comptrrefbase-class"></a>ComPtrRefBase 클래스

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

## <a name="syntax"></a>구문

```cpp
template <
   typename T
>
class ComPtrRefBase;
```

### <a name="parameters"></a>매개 변수

*T*<br/>
A [ComPtr\<T >](../windows/comptr-class.md) 형식 또는 형식에서 파생 하 여이 나타내는 인터페이스 뿐만 아니라는 `ComPtr`합니다.

## <a name="remarks"></a>설명

에 대 한 기본 클래스를 나타냅니다 합니다 [ComPtrRef](../windows/comptrref-class.md) 클래스입니다.

## <a name="members"></a>멤버

### <a name="public-typedefs"></a>공용 Typedefs

이름            | 설명
--------------- | -------------------------------------------------
`InterfaceType` | 템플릿 매개 변수의 형식에 대 한 동의어 *T*합니다.

### <a name="public-operators"></a>Public 연산자

이름                                                                       | 설명
-------------------------------------------------------------------------- | -----------------------------------------------------------------------------------------------------
[Comptrrefbase:: Operator IInspectable * *](#operator-iinspectable-star-star) | 현재 캐스팅 [ptr_](#ptr) 데이터 멤버는 포인터--a-포인터-을는 `IInspectable` 인터페이스입니다.
[Comptrrefbase:: Operator IUnknown * *](#operator-iunknown-star-star)         | 현재 캐스팅 [ptr_](#ptr) 데이터 멤버는 포인터--a-포인터-을는 `IUnknown` 인터페이스입니다.

### <a name="protected-data-members"></a>보호된 데이터 멤버

이름                        | 설명
--------------------------- | ----------------------------------------------------------------
[Comptrrefbase:: Ptr_](#ptr) | 현재 템플릿 매개 변수로 지정 된 형식에 대 한 포인터입니다.

## <a name="inheritance-hierarchy"></a>상속 계층

`ComPtrRefBase`

## <a name="requirements"></a>요구 사항

**헤더:** client.h

**Namespace:** Microsoft::WRL::Details

## <a name="operator-iinspectable-star-star"></a>Comptrrefbase:: Operator IInspectable\* \* 연산자

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

```cpp
operator IInspectable**() const;
```

### <a name="remarks"></a>설명

현재 캐스팅 [ptr_](#ptr) 데이터 멤버는 포인터--a-포인터-을는 `IInspectable` 인터페이스입니다.

오류가 발생 하는 경우에 내보내집니다 현재 `ComPtrRefBase` 에서 파생 되지 `IInspectable`합니다.

이 캐스트는 사용할 수 있는 경우에만 `__WRL_CLASSIC_COM__` 정의 됩니다.

## <a name="operator-iunknown-star-star"></a>Comptrrefbase:: Operator IUnknown * * 연산자

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

```cpp
operator IUnknown**() const;
```

### <a name="remarks"></a>설명

현재 캐스팅 [ptr_](#ptr) 데이터 멤버는 포인터--a-포인터-을는 `IUnknown` 인터페이스입니다.

오류가 발생 하는 경우에 내보내집니다 현재 `ComPtrRefBase` 에서 파생 되지 `IUnknown`합니다.

## <a name="ptr"></a>Comptrrefbase:: Ptr_

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

```cpp
T* ptr_;
```

### <a name="remarks"></a>설명

현재 템플릿 매개 변수로 지정 된 형식에 대 한 포인터입니다. `ptr_` 보호 된 데이터 멤버가입니다.
