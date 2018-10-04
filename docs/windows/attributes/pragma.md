---
title: pragma (c + + COM 특성) | Microsoft Docs
ms.custom: ''
ms.date: 10/02/2018
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- vc-attr.pragma
dev_langs:
- C++
helpviewer_keywords:
- pragma attribute
ms.assetid: 3f90d023-b8b5-4007-8311-008bb72cbea1
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 2d7f6b371db09fd5eac9d6ef7260df7d790c21df
ms.sourcegitcommit: 955ef0f9d966e7c9c65e040f1e28fa83abe102a5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48791186"
---
# <a name="pragma"></a>pragma

따옴표를 사용 하지 않고 생성 된.idl 파일에 지정된 된 문자열을 내보냅니다.

## <a name="syntax"></a>구문

```cpp
[ pragma(pragma_statement) ];
```

### <a name="parameters"></a>매개 변수

*pragma_statement*<br/>
생성 된.idl 파일로 이동 하려는 pragma입니다.

## <a name="remarks"></a>설명

합니다 **pragma** c + + 특성에 동일한 기능을 합니다 [pragma](/windows/desktop/Midl/pragma) MIDL 특성입니다.

## <a name="example"></a>예제

```cpp
// cpp_attr_ref_pragma.cpp
// compile with: /LD
#include "unknwn.h"
[module(name="MyLib")];
[pragma(pack(4))];

[dispinterface, uuid("00000000-0000-0000-0000-000000000001")]
__interface A
{
   [id(1)] HRESULT MyMethod ([in, satype("BSTR")] SAFEARRAY **p);
};
```

## <a name="requirements"></a>요구 사항

### <a name="attribute-context"></a>특성 컨텍스트

|||
|-|-|
|**적용 대상**|원하는 위치|
|**반복 가능**|아니요|
|**필수 특성**|없음|
|**잘못된 특성**|없음|

특성 컨텍스트에 대 한 자세한 내용은 참조 하세요. [특성 컨텍스트](cpp-attributes-com-net.md#contexts)합니다.

## <a name="see-also"></a>참고 항목

[IDL 특성](idl-attributes.md)<br/>
[독립 실행형 특성](stand-alone-attributes.md)<br/>
[pack](../../preprocessor/pack.md)  