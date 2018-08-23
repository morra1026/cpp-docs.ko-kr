---
title: AsyncResultType 열거형 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- async/Microsoft::WRL::AsyncResultType
dev_langs:
- C++
helpviewer_keywords:
- AsyncResultType enumeration
ms.assetid: 4195d234-3f3f-4363-9118-6ad2a7551cf2
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 2a79ef02302208aa14bc1620e486fcfbc6e12253
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42591265"
---
# <a name="asyncresulttype-enumeration"></a>AsyncResultType 열거형

반환 된 결과의 형식을 지정 합니다 `GetResults()` 메서드.

## <a name="syntax"></a>구문

```cpp
enum AsyncResultType;
```

## <a name="members"></a>멤버

### <a name="values"></a>값

|이름|설명|
|----------|-----------------|
|`MultipleResults`|간에 점진적으로 제공 되는 여러 결과 집합이 `Start` 상태 전과 `Close()` 라고 합니다.|
|`SingleResult`|후 제공 되는 단일 결과는 `Complete` 이벤트가 발생 합니다.|

## <a name="requirements"></a>요구 사항

**헤더:** async.h

**네임스페이스:** Microsoft::WRL

## <a name="see-also"></a>참고 항목

[Microsoft::WRL 네임스페이스](../windows/microsoft-wrl-namespace.md)