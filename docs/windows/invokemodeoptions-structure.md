---
title: InvokeModeOptions 구조체
ms.date: 03/22/2018
ms.topic: reference
f1_keywords:
- event/Microsoft::WRL::InvokeModeOptions
helpviewer_keywords:
- InvokeModeOptions structure
- InvokeMode enum
ms.openlocfilehash: 315f1f0c49c4222bf525bbaf25c9ad0de8b9c7d1
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50511700"
---
# <a name="invokemodeoptions-structure"></a>InvokeModeOptions 구조체

대리자 큐에서 모든 이벤트를 발생 시키는 아니면 오류가 발생 한 후 실행을 중지 하려면를 지정 합니다. 허용 되는 값은 지정 된 `InvokeMode` 열거형입니다.

## <a name="syntax"></a>구문

```cpp
enum InvokeMode
{
   StopOnFirstError = 1,
   FireAll = 2,
};

struct InvokeModeOptions
{
   static const InvokeMode invokeMode = invokeModeValue;
};
```

## <a name="requirements"></a>요구 사항

**헤더:** event.h

**네임스페이스:** Microsoft::WRL

## <a name="see-also"></a>참고 항목

[Microsoft::WRL 네임스페이스](../windows/microsoft-wrl-namespace.md)<br/>
[Microsoft::WRL::AgileEventSource 클래스](../windows/agileeventsource-class.md)