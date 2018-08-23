---
title: 'RoInitializeWrapper:: ~ RoInitializeWrapper 소멸자 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::RoInitializeWrapper::~RoInitializeWrapper
dev_langs:
- C++
ms.assetid: afef4c1f-ffde-4cd2-8654-8de4182eb5f4
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 5548eb413f0d5cd4c72983e00bdf65f61bb98f6d
ms.sourcegitcommit: 6f8dd98de57bb80bf4c9852abafef1c35a7600f1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/22/2018
ms.locfileid: "42597925"
---
# <a name="roinitializewrapperroinitializewrapper-destructor"></a>RoInitializeWrapper::~RoInitializeWrapper 소멸자

Windows 런타임 초기화를 취소 합니다.

## <a name="syntax"></a>구문

```cpp
~RoInitializeWrapper()  
```

## <a name="remarks"></a>설명

합니다 **RoInitializeWrapper** 클래스를 호출 `Windows::Foundation::Uninitialize()`합니다.

## <a name="requirements"></a>요구 사항

**헤더:** corewrappers.h

**Namespace:** Microsoft::WRL::Wrappers

## <a name="see-also"></a>참고 항목

[HandleT 클래스](../windows/handlet-class.md)