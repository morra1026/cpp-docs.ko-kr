---
title: RuntimeClassFlags 구조체 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::RuntimeClassFlags
dev_langs:
- C++
helpviewer_keywords:
- RuntimeClassFlags structure
ms.assetid: 7098d605-bd14-4d51-82f4-3def8296a938
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: f0a32fc373900af1a4322f4f2511c44417d2916a
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42594276"
---
# <a name="runtimeclassflags-structure"></a>RuntimeClassFlags 구조체

인스턴스에 대 한 형식이 포함 된 [RuntimeClass](../windows/runtimeclass-class.md)합니다.

## <a name="syntax"></a>구문

```cpp
template <
   unsigned int flags
>
struct RuntimeClassFlags;
```

### <a name="parameters"></a>매개 변수

*flags*  
A [RuntimeClassType 열거형](../windows/runtimeclasstype-enumeration.md) 값입니다.

## <a name="members"></a>멤버

### <a name="public-constants"></a>공용 상수

|이름|설명|
|----------|-----------------|
|[RuntimeClassFlags::value 상수](../windows/runtimeclassflags-value-constant.md)|포함 된 [RuntimeClassType 열거형](../windows/runtimeclasstype-enumeration.md) 값입니다.|

## <a name="inheritance-hierarchy"></a>상속 계층

`RuntimeClassFlags`

## <a name="requirements"></a>요구 사항

**헤더:** implements.h

**네임스페이스:** Microsoft::WRL

## <a name="see-also"></a>참고 항목

[Microsoft::WRL 네임스페이스](../windows/microsoft-wrl-namespace.md)