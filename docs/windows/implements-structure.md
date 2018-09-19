---
title: 구조를 구현 | Microsoft Docs
ms.custom: ''
ms.date: 09/11/2018
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::Implements
- implements/Microsoft::WRL::Implements::CanCastTo
- implements/Microsoft::WRL::Implements::CastToUnknown
- implements/Microsoft::WRL::Implements::FillArrayWithIid
- implements/Microsoft::WRL::Implements::IidCount
dev_langs:
- C++
helpviewer_keywords:
- Microsoft::WRL::Implements structure
- Microsoft::WRL::Implements::CanCastTo method
- Microsoft::WRL::Implements::CastToUnknown method
- Microsoft::WRL::Implements::FillArrayWithIid method
- Microsoft::WRL::Implements::IidCount method
ms.assetid: 29b13e90-34d4-4a0b-babd-5187c9eb0c36
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 18616b1010dfe6a23861c512b1113c30fe5251ce
ms.sourcegitcommit: b4432d30f255f0cb58dce69cbc8cbcb9d44bc68b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/13/2018
ms.locfileid: "45535355"
---
# <a name="implements-structure"></a>Implements 구조체

구현 `QueryInterface` 고 `GetIid` 지정된 된 인터페이스에 대 한 합니다.

## <a name="syntax"></a>구문

```cpp
template <
   typename I0,
   typename I1 = Details::Nil,
   typename I2 = Details::Nil,
   typename I3 = Details::Nil,
   typename I4 = Details::Nil,
   typename I5 = Details::Nil,
   typename I6 = Details::Nil,
   typename I7 = Details::Nil,
   typename I8 = Details::Nil,
   typename I9 = Details::Nil
>
struct __declspec(novtable) Implements : Details::ImplementsHelper<RuntimeClassFlags<WinRt>, typename Details::InterfaceListHelper<I0, I1, I2, I3, I4, I5, I6, I7, I8, I9>::TypeT>, Details::ImplementsBase;
template <
   int flags,
   typename I0,
   typename I1,
   typename I2,
   typename I3,
   typename I4,
   typename I5,
   typename I6,
   typename I7,
   typename I8
>
struct __declspec(novtable) Implements<RuntimeClassFlags<flags>, I0, I1, I2, I3, I4, I5, I6, I7, I8> : Details::ImplementsHelper<RuntimeClassFlags<flags>, typename Details::InterfaceListHelper<I0, I1, I2, I3, I4, I5, I6, I7, I8>::TypeT>, Details::ImplementsBase;
```

### <a name="parameters"></a>매개 변수

*I0*  
0 번째 인터페이스 id입니다. (필수)

*I1*  
첫 번째 인터페이스 id입니다. 이 매개 변수는 선택 사항입니다.

*I2*  
두 번째 인터페이스 id입니다. 이 매개 변수는 선택 사항입니다.

*I3*  
세 번째 인터페이스 id입니다. 이 매개 변수는 선택 사항입니다.

*I4*  
네 번째 인터페이스 id입니다. 이 매개 변수는 선택 사항입니다.

*I5*  
다섯 번째 인터페이스 id입니다. 이 매개 변수는 선택 사항입니다.

*I6*  
여섯 번째 인터페이스 id입니다. 이 매개 변수는 선택 사항입니다.

*I7*  
일곱 번째 인터페이스 id입니다. 이 매개 변수는 선택 사항입니다.

*I8*  
여덟 번째 인터페이스 id입니다. 이 매개 변수는 선택 사항입니다.

*I9*  
아홉 번째 인터페이스 id입니다. 이 매개 변수는 선택 사항입니다.

*flags*  
클래스에 대 한 구성 플래그입니다. 하나 이상의 [RuntimeClassType](../windows/runtimeclasstype-enumeration.md) 에 지정 된 열거형을 [RuntimeClassFlags](../windows/runtimeclassflags-structure.md) 구조입니다.

## <a name="remarks"></a>설명

지정 된 인터페이스 목록에서 파생 되며 구현에 대 한 도우미 템플릿을 `QueryInterface` 고 `GetIid`입니다.

각 *I0* 를 통해 *I9* 인터페이스 매개 변수 중 하나에서 파생 되어야 합니다 `IUnknown`를 `IInspectable`, 또는 [ChainInterfaces](../windows/chaininterfaces-structure.md) 템플릿. 합니다 *플래그* 매개 변수 지원에 대 한 생성 되는지 여부를 결정 `IUnknown` 또는 `IInspectable`합니다.

## <a name="members"></a>멤버

### <a name="public-typedefs"></a>공용 Typedefs

| 이름        | 설명                               |
| ----------- | ----------------------------------------- |
| `ClassFlags`| `RuntimeClassFlags<WinRt>`의 동의어입니다. |

### <a name="protected-methods"></a>보호된 메서드

| 이름                                              | 설명                                                                                                   |
| ------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| [Implements:: cancastto](#cancastto)               | 지정된 된 인터페이스에 대 한 포인터를 가져옵니다.                                                                    |
| [Implements:: casttounknown](#casttounknown)       | 기본 포인터를 가져옵니다 `IUnknown` 인터페이스입니다.                                                        |
| [Implements:: fillarraywithiid](#fillarraywithiid) | 현재 0 번째 템플릿 매개 변수로 지정 된 배열 요소에 지정 된 인터페이스 ID를 삽입 합니다. |

### <a name="protected-constants"></a>보호 된 상수

| 이름                              | 설명                                    |
| --------------------------------- | ---------------------------------------------- |
| [Implements:: iidcount](#iidcount) | 구현 된 인터페이스 Id 수를 보유합니다. |

## <a name="inheritance-hierarchy"></a>상속 계층

`I0`

`ChainInterfaces`

`I0`

`ImplementsBase`

`ImplementsHelper`

`Implements`

## <a name="requirements"></a>요구 사항

**헤더:** implements.h

**네임스페이스:** Microsoft::WRL

## <a name="cancastto"></a>Implements:: cancastto

지정된 된 인터페이스에 대 한 포인터를 가져옵니다.

```cpp
__forceinline HRESULT CanCastTo(
   REFIID riid,
   _Deref_out_ void **ppv
);
```

### <a name="parameters"></a>매개 변수

*riid*  
인터페이스 ID에 대 한 참조

*ppv*  
성공 하면 인터페이스에 대 한 포인터를 지정 *riid*합니다.

### <a name="return-value"></a>반환 값

성공 하면 s_ok이 고 그렇지 않으면 E_NOINTERFACE 같은 오류를 나타내는 HRESULT입니다.

### <a name="remarks"></a>설명

QueryInterface 작업을 수행 하는 내부 도우미 함수입니다.

## <a name="casttounknown"></a>Implements:: casttounknown

기본 포인터를 가져옵니다 `IUnknown` 인터페이스입니다.

```cpp
__forceinline IUnknown* CastToUnknown();
```

### <a name="return-value"></a>반환 값

이 작업에서 항상 성공 하 고 반환 된 `IUnknown` 포인터입니다.

### <a name="remarks"></a>설명

내부 도우미 함수입니다.

## <a name="fillarraywithiid"></a>Implements:: fillarraywithiid

현재 0 번째 템플릿 매개 변수로 지정 된 배열 요소에 지정 된 인터페이스 ID를 삽입 합니다.

```cpp
__forceinline static void FillArrayWithIid(
   unsigned long &index,
   _In_ IID* iids
);
```

### <a name="parameters"></a>매개 변수

*index*  
이 작업에 대 한 시작 배열 요소를 나타내는 0부터 시작 인덱스입니다. 이 작업이 완료 되 면 *인덱스* 1 씩 증가 합니다.

*iid*  
IID 형식의 배열입니다.

### <a name="remarks"></a>설명

내부 도우미 함수입니다.

## <a name="iidcount"></a>Implements:: iidcount

구현 된 인터페이스 Id 수를 보유합니다.

```cpp
static const unsigned long IidCount;
```
