---
title: RaiseException 함수 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- internal/Microsoft::WRL::Details::RaiseException
dev_langs:
- C++
helpviewer_keywords:
- RaiseException function
ms.assetid: f9c74f6d-112a-4d2e-900f-622f795d5dbf
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 49024e903237160cc26a9c095cf9f313b43ccb6f
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42600767"
---
# <a name="raiseexception-function"></a>RaiseException 함수

WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.

## <a name="syntax"></a>구문

```cpp
inline void __declspec(noreturn)   RaiseException(
      HRESULT hr,
      DWORD dwExceptionFlags = EXCEPTION_NONCONTINUABLE);
```

### <a name="parameters"></a>매개 변수

*hr*  
발생 중인 예외 예외 코드 HRESULT, 실패 한 작업입니다.

*dwExceptionFlags*  
건의 예외 (플래그 값이 0) 또는 noncontinuable 예외 (플래그 값은 0이 아닌)를 나타내는 플래그입니다. 기본적으로 예외는 계속할 수 없는입니다.

## <a name="remarks"></a>설명

호출 스레드에서 예외가 발생 합니다.

자세한 내용은 참조는 Windows `RaiseException` 함수입니다.

## <a name="requirements"></a>요구 사항

**헤더:** internal.h

**Namespace:** Microsoft::WRL::Details

## <a name="see-also"></a>참고 항목

[Microsoft::WRL::Details 네임스페이스](../windows/microsoft-wrl-details-namespace.md)