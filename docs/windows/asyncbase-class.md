---
title: AsyncBase 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 10/08/2018
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- async/Microsoft::WRL::AsyncBase
- async/Microsoft::WRL::AsyncBase::AsyncBase
- async/Microsoft::WRL::AsyncBase::Cancel
- async/Microsoft::WRL::AsyncBase::CheckValidStateForDelegateCall
- async/Microsoft::WRL::AsyncBase::CheckValidStateForResultsCall
- async/Microsoft::WRL::AsyncBase::Close
- async/Microsoft::WRL::AsyncBase::ContinueAsyncOperation
- async/Microsoft::WRL::AsyncBase::CurrentStatus
- async/Microsoft::WRL::AsyncBase::ErrorCode
- async/Microsoft::WRL::AsyncBase::FireCompletion
- async/Microsoft::WRL::AsyncBase::FireProgress
- async/Microsoft::WRL::AsyncBase::get_ErrorCode
- async/Microsoft::WRL::AsyncBase::get_Id
- async/Microsoft::WRL::AsyncBase::get_Status
- async/Microsoft::WRL::AsyncBase::GetOnComplete
- async/Microsoft::WRL::AsyncBase::GetOnProgress
- async/Microsoft::WRL::AsyncBase::OnCancel
- async/Microsoft::WRL::AsyncBase::OnClose
- async/Microsoft::WRL::AsyncBase::OnStart
- async/Microsoft::WRL::AsyncBase::put_Id
- async/Microsoft::WRL::AsyncBase::PutOnComplete
- async/Microsoft::WRL::AsyncBase::PutOnProgress
- async/Microsoft::WRL::AsyncBase::Start
- async/Microsoft::WRL::AsyncBase::TryTransitionToCompleted
- async/Microsoft::WRL::AsyncBase::TryTransitionToError
dev_langs:
- C++
helpviewer_keywords:
- Microsoft::WRL::AsyncBase class
- Microsoft::WRL::AsyncBase::AsyncBase, constructor
- Microsoft::WRL::AsyncBase::Cancel method
- Microsoft::WRL::AsyncBase::CheckValidStateForDelegateCall method
- Microsoft::WRL::AsyncBase::CheckValidStateForResultsCall method
- Microsoft::WRL::AsyncBase::Close method
- Microsoft::WRL::AsyncBase::ContinueAsyncOperation method
- Microsoft::WRL::AsyncBase::CurrentStatus method
- Microsoft::WRL::AsyncBase::ErrorCode method
- Microsoft::WRL::AsyncBase::FireCompletion method
- Microsoft::WRL::AsyncBase::FireProgress method
- Microsoft::WRL::AsyncBase::get_ErrorCode method
- Microsoft::WRL::AsyncBase::get_Id method
- Microsoft::WRL::AsyncBase::get_Status method
- Microsoft::WRL::AsyncBase::GetOnComplete method
- Microsoft::WRL::AsyncBase::GetOnProgress method
- Microsoft::WRL::AsyncBase::OnCancel method
- Microsoft::WRL::AsyncBase::OnClose method
- Microsoft::WRL::AsyncBase::OnStart method
- Microsoft::WRL::AsyncBase::put_Id method
- Microsoft::WRL::AsyncBase::PutOnComplete method
- Microsoft::WRL::AsyncBase::PutOnProgress method
- Microsoft::WRL::AsyncBase::Start method
- Microsoft::WRL::AsyncBase::TryTransitionToCompleted method
- Microsoft::WRL::AsyncBase::TryTransitionToError method
ms.assetid: 64259b9b-f427-4ffd-a611-e7a2f82362b2
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 9647e18af021caf67dea5d946c9e5bf00fb50807
ms.sourcegitcommit: 8480f16893f09911f08a58caf684405404f7ac8e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49162934"
---
# <a name="asyncbase-class"></a>AsyncBase 클래스

Windows 런타임 비동기 상태 컴퓨터를 구현합니다.

## <a name="syntax"></a>구문

```cpp
template <
    typename TComplete,
    typename TProgress = Details::Nil,
    AsyncResultType resultType = SingleResult
>
class AsyncBase : public AsyncBase<TComplete, Details::Nil, resultType>;

template <typename TComplete, AsyncResultType resultType>
class AsyncBase<TComplete, Details::Nil, resultType> :
    public Microsoft::WRL::Implements<IAsyncInfo>;
```

### <a name="parameters"></a>매개 변수

*TComplete*<br/>
비동기 작업이 완료 될 때 호출 되는 이벤트 처리기입니다.

*TProgress*<br/>
작업의 현재 진행률을 보고 하는 비동기 작업 실행을 때 호출 되는 이벤트 처리기입니다.

*resultType*<br/>
중 하나는 [AsyncResultType](../windows/asyncresulttype-enumeration.md) 열거형 값입니다. 기본적으로 `SingleResult`입니다.

## <a name="members"></a>멤버

### <a name="public-constructors"></a>Public 생성자

이름                               | 설명
---------------------------------- | -------------------------------------------------
[Asyncbase:: Asyncbase](#asyncbase) | `AsyncBase` 클래스의 인스턴스를 초기화합니다.

### <a name="public-methods"></a>Public 메서드

이름                                         | 설명
-------------------------------------------- | -------------------------------------------------------------------------------------
[Asyncbase:: Cancel](#cancel)                 | 비동기 작업을 취소합니다.
[Asyncbase:: Close](#close)                   | 비동기 작업을 닫습니다.
[Asyncbase:: Firecompletion](#firecompletion) | 완료 이벤트 처리기를 호출 하거나 내부 진행률 대리자를 다시 설정 합니다.
[Asyncbase:: Fireprogress](#fireprogress)     | 현재 진행률 이벤트 처리기를 호출합니다.
[Asyncbase:: Get_errorcode](#get-errorcode)   | 현재 비동기 작업에 대 한 오류 코드를 검색 합니다.
[Asyncbase:: Get_id](#get-id)                 | 비동기 작업의 핸들을 검색 합니다.
[Asyncbase:: Get_status](#get-status)         | 비동기 작업의 상태를 나타내는 값을 검색 합니다.
[Asyncbase:: Getoncomplete](#getoncomplete)   | 지정된 된 변수를 현재 완료 이벤트 처리기의 주소를 복사합니다.
[Asyncbase:: Getonprogress](#getonprogress)   | 지정된 된 변수를 현재 진행률 이벤트 처리기의 주소를 복사합니다.
[Asyncbase:: Put_id](#put-id)                 | 비동기 작업의 핸들을 설정 합니다.
[Asyncbase:: Putoncomplete](#putoncomplete)   | 완료 이벤트 처리기의 주소를 지정된 된 값으로 설정합니다.
[Asyncbase:: Putonprogress](#putonprogress)   | 진행률 이벤트 처리기의 주소를 지정된 된 값으로 설정합니다.
[Asyncbase:: Start](#start)                   | 비동기 작업을 시작 합니다.

### <a name="protected-methods"></a>보호된 메서드

이름                                                                         | 설명
---------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------
[Asyncbase:: Checkvalidstatefordelegatecall](#checkvalidstatefordelegatecall) | 현재 비동기 상태의 대리자 속성을 수정할 수 있는지 테스트 합니다.
[Asyncbase:: Checkvalidstateforresultscall](#checkvalidstateforresultscall)   | 현재 비동기 상태에서 비동기 작업의 결과 수집할 수 있는지 테스트 합니다.
[Asyncbase:: Continueasyncoperation](#continueasyncoperation)                 | 비동기 작업을 계속 처리 해야 중단 되어야 하는지 여부를 결정 합니다.
[Asyncbase:: Currentstatus](#currentstatus)                                   | 현재 비동기 작업의 상태를 검색합니다.
[Asyncbase:: Errorcode](#errorcode)                                           | 현재 비동기 작업에 대 한 오류 코드를 검색 합니다.
[Asyncbase:: Oncancel](#oncancel)                                             | 파생된 클래스에서 재정의 되 면 비동기 작업을 취소 합니다.
[Asyncbase:: Onclose](#onclose)                                               | 파생된 클래스에서 재정의 하는 경우 비동기 작업을 닫습니다.
[Asyncbase:: Onstart](#onstart)                                               | 파생된 클래스에서 재정의 되 면 비동기 작업을 시작 합니다.
[Asyncbase:: Trytransitiontocompleted](#trytransitiontocompleted)             | 현재 비동기 작업이 완료 되었는지 여부를 나타냅니다.
[Asyncbase:: Trytransitiontoerror](#trytransitiontoerror)                     | 지정된 된 오류 코드 내부 오류 상태를 수정할 수 있는지 여부를 나타냅니다.

## <a name="inheritance-hierarchy"></a>상속 계층

`AsyncBase`

`AsyncBase`

## <a name="requirements"></a>요구 사항

**헤더:** async.h

**네임스페이스:** Microsoft::WRL

## <a name="asyncbase"></a>Asyncbase:: Asyncbase

`AsyncBase` 클래스의 인스턴스를 초기화합니다.

```cpp
AsyncBase();
```

## <a name="cancel"></a>Asyncbase:: Cancel

비동기 작업을 취소합니다.

```cpp
STDMETHOD(
   Cancel
)(void);
```

### <a name="return-value"></a>반환 값

기본적으로 항상 S_OK를 반환합니다.

### <a name="remarks"></a>설명

`Cancel()` 기본 구현 이며 `IAsyncInfo::Cancel`, 없습니다 실제 작업을 수행 합니다. 비동기 작업을 실제로 취소 하려면 재정의 `OnCancel()` 순수 가상 메서드가 있습니다.

## <a name="checkvalidstatefordelegatecall"></a>Asyncbase:: Checkvalidstatefordelegatecall

현재 비동기 상태의 대리자 속성을 수정할 수 있는지 테스트 합니다.

```cpp
inline HRESULT CheckValidStateForDelegateCall();
```

### <a name="return-value"></a>반환 값

S_OK 대리자 속성을 수정할 수 있습니다. 그렇지 않으면 E_ILLEGAL_METHOD_CALL 합니다.

## <a name="checkvalidstateforresultscall"></a>Asyncbase:: Checkvalidstateforresultscall

현재 비동기 상태에서 비동기 작업의 결과 수집할 수 있는지 테스트 합니다.

```cpp
inline HRESULT CheckValidStateForResultsCall();
```

### <a name="return-value"></a>반환 값

S_OK 결과 수집할 수 있습니다. 그렇지 않으면 E_ILLEGAL_METHOD_CALLE_ILLEGAL_METHOD_CALL 합니다.

## <a name="close"></a>Asyncbase:: Close

비동기 작업을 닫습니다.

```cpp
STDMETHOD(
   Close
)(void) override;
```

### <a name="return-value"></a>반환 값

작업이 이미 닫히거나 경우 s_ok이 고, 닫혀 않으면 그렇지 않으면 E_ILLEGAL_STATE_CHANGE 합니다.

### <a name="remarks"></a>설명

`Close()` 기본 구현 이며 `IAsyncInfo::Close`, 없습니다 실제 작업을 수행 합니다. 비동기 작업을 실제로 닫으려면 재정의 `OnClose()` 순수 가상 메서드가 있습니다.

## <a name="continueasyncoperation"></a>Asyncbase:: Continueasyncoperation

비동기 작업을 계속 처리 해야 중단 되어야 하는지 여부를 결정 합니다.

```cpp
inline bool ContinueAsyncOperation();
```

### <a name="return-value"></a>반환 값

**true** 비동기 작업의 현재 상태 이면 *시작*, 즉, 작업을 계속 해야 합니다. 그렇지 않으면 **false**, 즉, 작업을 중지 해야 합니다.

## <a name="currentstatus"></a>Asyncbase:: Currentstatus

현재 비동기 작업의 상태를 검색합니다.

```cpp
inline void CurrentStatus(
   Details::AsyncStatusInternal *status
);
```

### <a name="parameters"></a>매개 변수

*status*<br/>
이 작업의 현재 상태를 저장 하는 위치를 위치입니다.

### <a name="remarks"></a>설명

이 작업은 스레드로부터 안전 합니다.

## <a name="errorcode"></a>Asyncbase:: Errorcode

현재 비동기 작업에 대 한 오류 코드를 검색 합니다.

```cpp
inline void ErrorCode(
   HRESULT *error
);
```

### <a name="parameters"></a>매개 변수

*error*<br/>
이 작업에서 현재 오류 코드를 저장 하는 위치를 위치입니다.

### <a name="remarks"></a>설명

이 작업은 스레드로부터 안전 합니다.

## <a name="firecompletion"></a>Asyncbase:: Firecompletion

완료 이벤트 처리기를 호출 하거나 내부 진행률 대리자를 다시 설정 합니다.

```cpp
void FireCompletion(
   void
) override;

virtual void FireCompletion();
```

### <a name="remarks"></a>설명

첫 번째 버전 `FireCompletion()` 내부 진행률 대리자 변수를 다시 설정 합니다. 비동기 작업이 완료 될 경우 완료 이벤트 처리기를 호출 하는 두 번째 버전입니다.

## <a name="fireprogress"></a>Asyncbase:: Fireprogress

현재 진행률 이벤트 처리기를 호출합니다.

```cpp
void FireProgress(
   const typename ProgressTraits::Arg2Type arg
);
```

### <a name="parameters"></a>매개 변수

*arg*<br/>
이벤트 처리기 메서드를 호출 합니다.

### <a name="remarks"></a>설명

`ProgressTraits` 파생 됩니다 [ArgTraitsHelper 구조체](../windows/argtraitshelper-structure.md)합니다.

## <a name="get-errorcode"></a>Asyncbase:: Get_errorcode

현재 비동기 작업에 대 한 오류 코드를 검색 합니다.

```cpp
STDMETHOD(
   get_ErrorCode
)(HRESULT* errorCode) override;
```

### <a name="parameters"></a>매개 변수

*오류 코드*<br/>
현재 오류 코드가 저장 된 위치입니다.

### <a name="return-value"></a>반환 값

성공 하면 s_ok이 고 그렇지 않으면 현재 비동기 작업이 닫히면 E_ILLEGAL_METHOD_CALL 합니다.

## <a name="get-id"></a>Asyncbase:: Get_id

비동기 작업의 핸들을 검색 합니다.

```cpp
STDMETHOD(
   get_Id
)(unsigned int *id) override;
```

### <a name="parameters"></a>매개 변수

*ID*<br/>
핸들이 저장할 수 있는 위치입니다.

### <a name="return-value"></a>반환 값

성공 하면 s_ok이 고 그렇지 않으면 E_ILLEGAL_METHOD_CALL 합니다.

### <a name="remarks"></a>설명

이 메서드는 `IAsyncInfo::get_Id`를 구현합니다.

## <a name="get-status"></a>Asyncbase:: Get_status

비동기 작업의 상태를 나타내는 값을 검색 합니다.

```cpp
STDMETHOD(
   get_Status
)(AsyncStatus *status) override;
```

### <a name="parameters"></a>매개 변수

*status*<br/>
상태를 저장할 위치입니다. 자세한 내용은 참조 하세요. `Windows::Foundation::AsyncStatus` 열거형입니다.

### <a name="return-value"></a>반환 값

성공 하면 s_ok이 고 그렇지 않으면 E_ILLEGAL_METHOD_CALL 합니다.

### <a name="remarks"></a>설명

이 메서드는 `IAsyncInfo::get_Status`를 구현합니다.

## <a name="getoncomplete"></a>Asyncbase:: Getoncomplete

지정된 된 변수를 현재 완료 이벤트 처리기의 주소를 복사합니다.

```cpp
STDMETHOD(
   GetOnComplete
)(TComplete** completeHandler);
```

### <a name="parameters"></a>매개 변수

*completeHandler*<br/>
현재 완료 이벤트 처리기의 주소를 저장 된 위치입니다.

### <a name="return-value"></a>반환 값

성공 하면 s_ok이 고 그렇지 않으면 E_ILLEGAL_METHOD_CALL 합니다.

## <a name="getonprogress"></a>Asyncbase:: Getonprogress

지정된 된 변수를 현재 진행률 이벤트 처리기의 주소를 복사합니다.

```cpp
STDMETHOD(
   GetOnProgress
)(TProgress** progressHandler);
```

### <a name="parameters"></a>매개 변수

*progressHandler*<br/>
현재 진행률 이벤트 처리기의 주소를 저장 된 위치입니다.

### <a name="return-value"></a>반환 값

성공 하면 s_ok이 고 그렇지 않으면 E_ILLEGAL_METHOD_CALL 합니다.

## <a name="oncancel"></a>Asyncbase:: Oncancel

파생된 클래스에서 재정의 되 면 비동기 작업을 취소 합니다.

```cpp
virtual void OnCancel(
   void
) = 0;
```

## <a name="onclose"></a>Asyncbase:: Onclose

파생된 클래스에서 재정의 하는 경우 비동기 작업을 닫습니다.

```cpp
virtual void OnClose(
   void
) = 0;
```

## <a name="onstart"></a>Asyncbase:: Onstart

파생된 클래스에서 재정의 되 면 비동기 작업을 시작 합니다.

```cpp
virtual HRESULT OnStart(
   void
) = 0;
```

## <a name="put-id"></a>Asyncbase:: Put_id

비동기 작업의 핸들을 설정 합니다.

```cpp
STDMETHOD(
   put_Id
)(const unsigned int id);
```

### <a name="parameters"></a>매개 변수

*ID*<br/>
0이 아닌 핸들입니다.

### <a name="return-value"></a>반환 값

성공 하면 s_ok이 고 이 고, 그렇지 E_INVALIDARG 또는 E_ILLEGAL_METHOD_CALL 합니다.

## <a name="putoncomplete"></a>Asyncbase:: Putoncomplete

완료 이벤트 처리기의 주소를 지정된 된 값으로 설정합니다.

```cpp
STDMETHOD(
   PutOnComplete
)(TComplete* completeHandler);
```

### <a name="parameters"></a>매개 변수

*completeHandler*<br/>
완료 이벤트 처리기에 설정 된 주소입니다.

### <a name="return-value"></a>반환 값

성공 하면 s_ok이 고 그렇지 않으면 E_ILLEGAL_METHOD_CALL 합니다.

## <a name="putonprogress"></a>Asyncbase:: Putonprogress

진행률 이벤트 처리기의 주소를 지정된 된 값으로 설정합니다.

```cpp
STDMETHOD(
   PutOnProgress
)(TProgress* progressHandler);
```

### <a name="parameters"></a>매개 변수

*progressHandler*<br/>
진행률 이벤트 처리기에 설정 된 주소입니다.

### <a name="return-value"></a>반환 값

성공 하면 s_ok이 고 그렇지 않으면 E_ILLEGAL_METHOD_CALL 합니다.

## <a name="start"></a>Asyncbase:: Start

비동기 작업을 시작 합니다.

```cpp
STDMETHOD(
   Start
)(void);
```

### <a name="return-value"></a>반환 값

S_ok이 고, 작업을 시작 하거나 이미 있는 경우 시작 합니다. 그렇지 않으면 E_ILLEGAL_STATE_CHANGE 합니다.

### <a name="remarks"></a>설명

`Start()` 기본 구현 이며 `IAsyncInfo::Start`, 없습니다 실제 작업을 수행 합니다. 실제로 비동기 작업을 시작 하려면 재정의 `OnStart()` 순수 가상 메서드가 있습니다.

## <a name="trytransitiontocompleted"></a>Asyncbase:: Trytransitiontocompleted

현재 비동기 작업이 완료 되었는지 여부를 나타냅니다.

```cpp
bool TryTransitionToCompleted(
   void
);
```

### <a name="return-value"></a>반환 값

**true 이면** 비동기 작업이 완료 되었으면;이 고, 그렇지 **false**합니다.

## <a name="trytransitiontoerror"></a>Asyncbase:: Trytransitiontoerror

지정된 된 오류 코드 내부 오류 상태를 수정할 수 있는지 여부를 나타냅니다.

```cpp
bool TryTransitionToError(
   const HRESULT error
);
```

### <a name="parameters"></a>매개 변수

*error*<br/>
HRESULT 오류가 발생 합니다.

### <a name="return-value"></a>반환 값

**true 이면** 내부 오류 상태가 고, 그렇지 않으면 변경 되었으면 **false**합니다.

### <a name="remarks"></a>설명

오류 상태는 s_ok가 이미 설정 되어 있는 경우에이 작업은 오류 상태를 수정 합니다. 이 작업이 오류 상태가 이미 오류, 취소, 완료 또는 종료 하는 경우에 효과가 없습니다.
