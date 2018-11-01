---
title: RaiseException 함수
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- internal/Microsoft::WRL::Details::RaiseException
helpviewer_keywords:
- RaiseException function
ms.assetid: f9c74f6d-112a-4d2e-900f-622f795d5dbf
ms.openlocfilehash: af0b35e1014f79c7907711b95200c241d31b6117
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50594755"
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

*hr*<br/>
발생 중인 예외 예외 코드 HRESULT, 실패 한 작업입니다.

*dwExceptionFlags*<br/>
건의 예외 (플래그 값이 0) 또는 noncontinuable 예외 (플래그 값은 0이 아닌)를 나타내는 플래그입니다. 기본적으로 예외는 계속할 수 없는입니다.

## <a name="remarks"></a>설명

호출 스레드에서 예외가 발생 합니다.

자세한 내용은 참조는 Windows `RaiseException` 함수입니다.

## <a name="requirements"></a>요구 사항

**헤더:** internal.h

**Namespace:** Microsoft::WRL::Details

## <a name="see-also"></a>참고 항목

[Microsoft::WRL::Details 네임스페이스](../windows/microsoft-wrl-details-namespace.md)