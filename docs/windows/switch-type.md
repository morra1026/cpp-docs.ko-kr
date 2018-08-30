---
title: switch_type | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- vc-attr.switch_type
dev_langs:
- C++
helpviewer_keywords:
- switch_type attribute
ms.assetid: e24544dc-b3bc-48ae-b249-f967db49271e
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: faa2a3be7260eecb16599db967336bcb7b774c99
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43200128"
---
# <a name="switchtype"></a>switch_type

Union 판별으로 사용 된 변수의 형식을 식별 합니다.

## <a name="syntax"></a>구문

```cpp
[switch_type(
type
}]
```

### <a name="parameters"></a>매개 변수

*type*  
스위치 형식이 정수, 문자, 부울, 또는 열거형 형식 수 있습니다.

## <a name="remarks"></a>설명

합니다 **switch_type** c + + 특성에 동일한 기능을 합니다 [switch_type](/windows/desktop/Midl/switch-type) MIDL 특성입니다.

C + + 특성을 지원 하지 않습니다 [공용 구조체를 캡슐화](/windows/desktop/Midl/encapsulated-unions)합니다. [공용 구조체 nonencapsulated](/windows/desktop/Midl/nonencapsulated-unions) 다음과 같은 형식 에서만 지원 됩니다.

```cpp
// cpp_attr_ref_switch_type.cpp
// compile with: /LD
#include <windows.h>
[module(name="MyLibrary")];
[ export ]
struct SizedValue2 {
   [switch_type("char"), switch_is(kind)] union {
      [case(1), string]
         wchar_t* wval;
      [default, string]
         char* val;
   };
   char kind;
};
```

## <a name="example"></a>예제

참조 된 [사례](../windows/case-cpp.md) 의 샘플 사용에 대 한 예제 **switch_type**합니다.

## <a name="requirements"></a>요구 사항

### <a name="attribute-context"></a>특성 컨텍스트

|||
|-|-|
|**적용 대상**|**typedef**|
|**반복 가능**|아니요|
|**필수 특성**|없음|
|**잘못된 특성**|없음|

특성 컨텍스트에 대한 자세한 내용은 [특성 컨텍스트](../windows/attribute-contexts.md)를 참조하세요.

## <a name="see-also"></a>참고 항목

[IDL 특성](../windows/idl-attributes.md)  
[Typedef, Enum, Union 및 Struct 특성](../windows/typedef-enum-union-and-struct-attributes.md)  
[export](../windows/export.md)  