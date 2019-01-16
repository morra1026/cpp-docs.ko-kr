---
title: CancelTransitionPolicy 열거형
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::CancelTransitionPolicy::TransitionFromCanceled
- module/Microsoft::WRL::CancelTransitionPolicy::RemainCanceled
- module/Microsoft::WRL::CancelTransitionPolicy
helpviewer_keywords:
- CancelTransitionPolicy Enumeration
ms.assetid: 5de49f7d-e5e3-43e9-bbca-666caf226cef
ms.openlocfilehash: cfd8e25f98ec1001a8fbd287eaec12408b9f240e
ms.sourcegitcommit: 360b55e89e5954f494e52b1cf989fbaceda06f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54336481"
---
# <a name="canceltransitionpolicy-enumeration"></a>CancelTransitionPolicy 열거형

비동기 작업의 터미널 상태로 전환 하려고 하는 방법을 나타냅니다 완료 또는 오류는 클라이언트 요청 취소 상태와 관련 하 여 작동 해야 합니다.

## <a name="syntax"></a>구문

```cpp
enum CancelTransitionPolicy;
```

## <a name="members"></a>멤버

### <a name="values"></a>값

|이름|설명|
|----------|-----------------|
|`RemainCanceled`|비동기 작업에 현재 클라이언트 요청 취소 된 상태로 터미널 완료 또는 오류 상태를 전환 하는 대신 취소 된 상태로 남아 있는지 나타냅니다.|
|`TransitionFromCanceled`|비동기 작업을 현재 클라이언트 요청 취소 된 상태로 있는 경우 취소 된 상태로 터미널 상태에 완료 된 상태로 전환 해야 나타냅니다 또는 오류가이 플래그를 사용 하는 호출을 기준으로 합니다.|

## <a name="requirements"></a>요구 사항

**헤더:** async.h

**네임스페이스:** Microsoft::WRL

## <a name="see-also"></a>참고 항목

[Microsoft::WRL 네임스페이스](microsoft-wrl-namespace.md)