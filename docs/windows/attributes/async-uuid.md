---
title: async_uuid (c + + COM 특성) | Microsoft Docs
ms.custom: ''
ms.date: 10/02/2018
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- vc-attr.async_uuid
dev_langs:
- C++
helpviewer_keywords:
- async_uuid attribute
ms.assetid: 235cb0d7-be58-4dd9-983c-e2a21bbc42c6
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 336bbf00edc84335972171aba0e7fc01e206984e
ms.sourcegitcommit: 955ef0f9d966e7c9c65e040f1e28fa83abe102a5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48791345"
---
# <a name="asyncuuid"></a>async_uuid

MIDL 컴파일러에 지시 합니다 COM 인터페이스의 동기 및 비동기 버전을 정의 하는 UUID를 지정 합니다.

## <a name="syntax"></a>구문

```cpp
[async_uuid (uuid)]
```

### <a name="parameters"></a>매개 변수

*uuid*<br/>
인터페이스의 버전을 식별 하는 UUID입니다.

## <a name="remarks"></a>설명

합니다 **async_uuid** c + + 특성에 동일한 기능을 합니다 [async_uuid](/windows/desktop/Midl/async-uuid) MIDL 특성입니다.

## <a name="example"></a>예제

```cpp
// cpp_attr_ref_async_uuid.cpp
// compile with: /LD
#include <Windows.h>
[module(name="Test")];
[object, uuid("9e66a290-4365-11d2-a997-00c04fa37ddb"),
async_uuid("e8583106-38fd-487e-912e-4fc8645c677e")]
__interface ICustom {
   HRESULT Custom([in] long l, [out, retval] long *pLong);
};
```

## <a name="requirements"></a>요구 사항

### <a name="attribute-context"></a>특성 컨텍스트

|||
|-|-|
|**적용 대상**|`interface`|
|**반복 가능**|아니요|
|**필수 특성**|없음|
|**잘못된 특성**|**이중**, **dispinterface**|

특성 컨텍스트에 대 한 자세한 내용은 참조 하세요. [특성 컨텍스트](cpp-attributes-com-net.md#contexts)합니다.

## <a name="see-also"></a>참고 항목

[IDL 특성](idl-attributes.md)<br/>
[인터페이스 특성](interface-attributes.md)  