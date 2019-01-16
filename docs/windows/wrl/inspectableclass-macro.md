---
title: InspectableClass 매크로
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- implements/Microsoft::WRL::InspectableClass
ms.assetid: ff390b26-58cc-424f-87ac-1fe3cc692b59
ms.openlocfilehash: bdc3dc5b54aa28280f22b1481a9be20ee0be22c6
ms.sourcegitcommit: 360b55e89e5954f494e52b1cf989fbaceda06f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54336761"
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

*runtimeClassName*<br/>
런타임 클래스의 전체 텍스트 이름입니다.

*trustLevel*<br/>
중 하나는 [TrustLevel](https://msdn.microsoft.com/library/br224625.aspx) 열거형 값입니다.

## <a name="remarks"></a>설명

합니다 **InspectableClass** 매크로 Windows 런타임 형식에만 사용할 수 있습니다.

## <a name="requirements"></a>요구 사항

**헤더:** implements.h

**네임스페이스:** Microsoft::WRL

## <a name="see-also"></a>참고 항목

[RuntimeClass 클래스](runtimeclass-class.md)