---
title: InspectableClass 매크로 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::InspectableClass
dev_langs:
- C++
ms.assetid: ff390b26-58cc-424f-87ac-1fe3cc692b59
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 9b85a10c68b7379f0e59bf859b3d8badf7413195
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43208343"
---
# <a name="inspectableclass-macro"></a>InspectableClass 매크로

런타임 클래스 이름 및 신뢰 수준을 설정합니다.

## <a name="syntax"></a>구문

```cpp
InspectableClass(
   runtimeClassName,
   trustLevel)  
```

### <a name="parameters"></a>매개 변수

*runtimeClassName*  
런타임 클래스의 전체 텍스트 이름입니다.

*trustLevel*  
중 하나는 [TrustLevel](https://msdn.microsoft.com/library/br224625.aspx) 열거형 값입니다.

## <a name="remarks"></a>설명

합니다 **InspectableClass** 매크로 Windows 런타임 형식에만 사용할 수 있습니다.

## <a name="requirements"></a>요구 사항

**헤더:** implements.h

**네임스페이스:** Microsoft::WRL

## <a name="see-also"></a>참고 항목

[RuntimeClass 클래스](../windows/runtimeclass-class.md)