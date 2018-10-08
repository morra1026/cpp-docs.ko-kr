---
title: requires_category (c + + COM 특성) | Microsoft Docs
ms.custom: ''
ms.date: 10/02/2018
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- vc-attr.requires_category
dev_langs:
- C++
helpviewer_keywords:
- requires_category attribute
ms.assetid: a645fdc6-1ef5-414d-8c56-5fe2686d4687
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 61743dfdb5eb684cbf09705ace4ce2531c292ff4
ms.sourcegitcommit: 955ef0f9d966e7c9c65e040f1e28fa83abe102a5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/04/2018
ms.locfileid: "48791279"
---
# <a name="requirescategory"></a>requires_category

대상 클래스의 필수 구성 요소 범주를 지정합니다.

## <a name="syntax"></a>구문

```cpp
[ requires_category(
  requires_category) ]
```

### <a name="parameters"></a>매개 변수

*requires_category*<br/>
필요한 범주의 ID입니다.

## <a name="remarks"></a>설명

합니다 **requires_category** c + + 특성 대상 클래스에 필요한 구성 요소 범주를 지정 합니다. 자세한 내용은 [REQUIRED_CATEGORY](../../atl/reference/category-macros.md#required_category)합니다.

이 특성을 사용 하려면 합니다 [coclass](coclass.md)를 [progid](progid.md), 또는 [vi_progid](vi-progid.md) 특성 (또는 다음 중 하나를 암시 하는 다른 특성)도 적용할 같은 요소입니다.

## <a name="example"></a>예제

다음 코드는 개체 컨트롤 범주를 구현 하는 필요 합니다.

```cpp
// cpp_attr_ref_requires_category.cpp
// compile with: /LD
#define _ATL_ATTRIBUTES
#include "atlbase.h"
#include "atlcom.h"

[module (name="MyLibrary")];

[ coclass, requires_category("CATID_Control"),
  uuid("1e1a2436-f3ea-4ff3-80bf-5409370e8144")]
class CMyClass {};
```

## <a name="requirements"></a>요구 사항

### <a name="attribute-context"></a>특성 컨텍스트

|||
|-|-|
|**적용 대상**|**클래스**, **구조체**|
|**반복 가능**|아니요|
|**필수 특성**|다음 중 하나 이상의: `coclass`, `progid`, 또는 `vi_progid`합니다.|
|**잘못된 특성**|없음|

특성 컨텍스트에 대 한 자세한 내용은 참조 하세요. [특성 컨텍스트](cpp-attributes-com-net.md#contexts)합니다.

## <a name="see-also"></a>참고 항목

[COM 특성](com-attributes.md)<br/>
[implements_category](implements-category.md)  