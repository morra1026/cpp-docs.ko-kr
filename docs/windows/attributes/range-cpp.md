---
title: 범위 (c + + COM 특성) | Microsoft Docs
ms.custom: ''
ms.date: 10/02/2018
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- vc-attr.range
dev_langs:
- C++
helpviewer_keywords:
- range attribute
ms.assetid: f352f79e-ecb3-4cdd-9cdd-8406ef473594
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 593cfbd4b7430c3f6ac5b4f2ab1053665136ab25
ms.sourcegitcommit: 955ef0f9d966e7c9c65e040f1e28fa83abe102a5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48791159"
---
# <a name="range-c"></a>range(C++)

인수 값은 런타임에 설정 된 필드에 허용 되는 값의 범위를 지정 합니다.

## <a name="syntax"></a>구문

```cpp
[ range(low, high) ]
```

### <a name="parameters"></a>매개 변수

*low*<br/>
하위 범위의 값입니다.

*high*<br/>
범위 상한 값입니다.

## <a name="remarks"></a>설명

합니다 **범위** c + + 특성에 동일한 기능을 합니다 [범위](/windows/desktop/Midl/range) MIDL 특성입니다.

## <a name="example"></a>예제

```cpp
// cpp_attr_ref_range.cpp
// compile with: /LD
#include <unknwn.h>
[module(name="MyLib")];

[object, uuid("9E66A290-4365-11D2-A997-00C04FA37DDB")]
__interface ICustom {
   HRESULT Custom([in] long l, [out, retval] long *pLong);
   HRESULT length_is1([in, range(0, 999)] long f, [in, length_is(f)] char array[10]);
   HRESULT length_is2([in, range(-99, -1)] long f, [in, length_is("f"), size_is(10)] char *array);
};
```

## <a name="requirements"></a>요구 사항

### <a name="attribute-context"></a>특성 컨텍스트

|||
|-|-|
|**적용 대상**|인터페이스 메서드를 인터페이스 매개 변수|
|**반복 가능**|아니요|
|**필수 특성**|없음|
|**잘못된 특성**|없음|

특성 컨텍스트에 대 한 자세한 내용은 참조 하세요. [특성 컨텍스트](cpp-attributes-com-net.md#contexts)합니다.

## <a name="see-also"></a>참고 항목

[IDL 특성](idl-attributes.md)<br/>
[메서드 특성](method-attributes.md)<br/>
[매개 변수 특성](parameter-attributes.md)<br/>
[데이터 멤버 특성](data-member-attributes.md)  