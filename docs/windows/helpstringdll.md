---
title: helpstringdll | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- vc-attr.helpstringdll
dev_langs:
- C++
helpviewer_keywords:
- helpstringdll attribute [C++]
ms.assetid: 121271fa-f061-492b-b87f-bbfcf4b02e7b
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 1eecedca8988c95466a3f257fbc77768b7c67b3b
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46392868"
---
# <a name="helpstringdll"></a>typelib

문서 문자열 조회 (지역화)를 수행 하는 데 DLL의 이름을 지정 합니다.

## <a name="syntax"></a>구문

```cpp
[ helpstringdll(
   "string"
) ]
```

### <a name="parameters"></a>매개 변수

*string*<br/>
문서 문자열 조회를 수행 하는 데 DLL입니다.

## <a name="remarks"></a>설명

합니다 **helpstringdll** c + + 특성에 동일한 기능을 합니다 [helpstringdll](/windows/desktop/Midl/helpstringdll) MIDL 특성입니다.

## <a name="example"></a>예제

```cpp
// cpp_attr_ref_helpstringdll.cpp
// compile with: /LD
#include <unknwn.h>
[module(name="MyLib", helpstringdll="xx.dll")];

[object, uuid("00000000-0000-0000-0000-000000000001")]
__interface IMyI
{
   HRESULT xxx();
};
```

## <a name="requirements"></a>요구 사항

### <a name="attribute-context"></a>특성 컨텍스트

|||
|-|-|
|**적용 대상**|**클래스**하십시오 **인터페이스**, 인터페이스 메서드|
|**반복 가능**|아니요|
|**필수 특성**|없음|
|**잘못된 특성**|없음|

자세한 내용은 [특성 컨텍스트](../windows/attribute-contexts.md)를 참조하세요.

## <a name="see-also"></a>참고 항목

[IDL 특성](../windows/idl-attributes.md)<br/>
[인터페이스 특성](../windows/interface-attributes.md)<br/>
[클래스 특성](../windows/class-attributes.md)<br/>
[메서드 특성](../windows/method-attributes.md)  