---
title: AsWeak 함수
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- client/Microsoft::WRL::AsWeak
helpviewer_keywords:
- AsWeak function
ms.assetid: a6f10cfc-c1d6-4761-adb9-1a119cc99913
ms.openlocfilehash: 1332aa140a8298590ad83158e0ec1b75035c4e92
ms.sourcegitcommit: 360b55e89e5954f494e52b1cf989fbaceda06f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54337375"
---
# <a name="asweak-function"></a>AsWeak 함수

지정된 인스턴스에 대한 약한 참조를 가져옵니다.

## <a name="syntax"></a>구문

```cpp
template<typename T>
HRESULT AsWeak(
   _In_ T* p,
   _Out_ WeakRef* pWeak
);
```

### <a name="parameters"></a>매개 변수

*T*<br/>
매개 변수의 형식에 대 한 포인터 *p*합니다.

*p*<br/>
형식의 인스턴스입니다.

*pWeak*<br/>
이 작업이 완료 되 면 매개 변수에 대 한 약한 참조에 대 한 포인터 *p*합니다.

## <a name="return-value"></a>반환 값

이 작업에 성공 하면 S_OK 그렇지 않으면 실패의 원인을 나타내는 HRESULT 오류가 발생 합니다.

## <a name="requirements"></a>요구 사항

**헤더:** client.h

**네임스페이스:** Microsoft::WRL

## <a name="see-also"></a>참고 항목

[Microsoft::WRL 네임스페이스](microsoft-wrl-namespace.md)