---
title: GetModuleBase 함수 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::GetModuleBase
dev_langs:
- C++
ms.assetid: 123d3b14-2eaf-4e02-8dcd-b6567917c6a6
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: afa76ad23c509689dd693bb0f3e13dbb7adb4d54
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50075452"
---
# <a name="getmodulebase-function"></a>GetModuleBase 함수
검색을 [ModuleBase](../windows/modulebase-class.md) 포인터의 참조 횟수를 증가 및 감소를 허용 하는 [RuntimeClass](../windows/runtimeclass-class.md) 개체입니다.

## <a name="syntax"></a>구문

```cpp
inline Details::ModuleBase* GetModuleBase() throw()
```

## <a name="return-value"></a>반환 값

`ModuleBase` 개체에 대한 포인터입니다.

## <a name="remarks"></a>설명

이 함수는 데 내부적으로 증가 및 감소 개체 참조를 계산 합니다.

호출 하 여 참조 횟수를 제어 하려면이 함수를 사용할 수 있습니다 [modulebase:: Incrementobjectcount](../windows/modulebase-incrementobjectcount-method.md) 하 고 [modulebase:: Decrementobjectcount](../windows/modulebase-decrementobjectcount-method.md)합니다.

## <a name="requirements"></a>요구 사항

**헤더:** implements.h

**네임스페이스:** Microsoft::WRL

## <a name="see-also"></a>참고 항목

[Microsoft::WRL 네임스페이스](../windows/microsoft-wrl-namespace.md)