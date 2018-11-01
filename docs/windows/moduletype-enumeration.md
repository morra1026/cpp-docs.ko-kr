---
title: ModuleType 열거형
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::ModuleType
helpviewer_keywords:
- ModuleType enumeration
ms.assetid: 61a763af-a5a4-451d-8b40-815af507fcde
ms.openlocfilehash: d822d214d9bad564286cd2c7494c9f480abdcf00
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50524750"
---
# <a name="moduletype-enumeration"></a>ModuleType 열거형

모듈이 in-process 서버를 지원하는지 out-of-process 서버를 지원해야 하는지 여부를 지정합니다.

## <a name="syntax"></a>구문

```cpp
enum ModuleType;
```

## <a name="members"></a>멤버

### <a name="values"></a>값

|이름|설명|
|----------|-----------------|
|`InProc`|in-process 서버입니다.|
|`OutOfProc`|-out-of-process 서버입니다.|
|`DisableCaching`|모듈에 캐싱 메커니즘을 사용 하지 않도록 설정 합니다.|
|`InProcDisableCaching`|조합 `InProc` 고 `DisableCaching`입니다.|
|`OutOfProcDisableCaching`|조합 `OutOfProc` 고 `DisableCaching`입니다.|

## <a name="requirements"></a>요구 사항

**헤더:** module.h

**네임스페이스:** Microsoft::WRL

## <a name="see-also"></a>참고 항목

[Microsoft::WRL 네임스페이스](../windows/microsoft-wrl-namespace.md)