---
title: unique (c + + COM 특성)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.unique
helpviewer_keywords:
- unique attribute
ms.assetid: abd7ed14-5ae7-44a8-8333-0058e9c92b2f
ms.openlocfilehash: 9d049983bb072e073180f1821f04b79e5f5c7444
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50512837"
---
# <a name="unique-c"></a>unique(C++)

고유 포인터를 지정합니다.

## <a name="syntax"></a>구문

```cpp
[unique]
```

## <a name="remarks"></a>설명

합니다 **고유** c + + 특성에 동일한 기능을 합니다 [고유](/windows/desktop/Midl/unique) MIDL 특성입니다.

## <a name="example"></a>예제

참조 된 [ref](ref-cpp.md) 의 샘플 사용에 대 한 예제 **고유**합니다.

## <a name="requirements"></a>요구 사항

### <a name="attribute-context"></a>특성 컨텍스트

|||
|-|-|
|**적용 대상**|**typedef**하십시오 **구조체**, **union**인터페이스 매개 변수, 인터페이스 메서드|
|**반복 가능**|아니요|
|**필수 특성**|없음|
|**잘못된 특성**|없음|

특성 컨텍스트에 대한 자세한 내용은 [특성 컨텍스트](cpp-attributes-com-net.md#contexts)를 참조하세요.

## <a name="see-also"></a>참고 항목

[IDL 특성](idl-attributes.md)<br/>
[Typedef, Enum, Union 및 Struct 특성](typedef-enum-union-and-struct-attributes.md)<br/>
[매개 변수 특성](parameter-attributes.md)