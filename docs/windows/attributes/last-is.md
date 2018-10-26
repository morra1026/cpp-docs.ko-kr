---
title: last_is (c + + COM 특성) | Microsoft Docs
ms.custom: ''
ms.date: 10/02/2018
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- vc-attr.last_is
dev_langs:
- C++
helpviewer_keywords:
- last_is attribute
ms.assetid: 9e045ac0-fa38-4249-af55-67bde5d0a58c
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 45b55886512c411cf82fe30c94b8d5087a811ad7
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50053632"
---
# <a name="lastis"></a>last_is

전송할 마지막 배열 요소의 인덱스를 지정 합니다.

## <a name="syntax"></a>구문

```cpp
[ last_is("expression") ]
```

### <a name="parameters"></a>매개 변수

*식*<br/>
하나 이상의 C 언어 식입니다. 빈 인수 슬롯 허용 됩니다.

## <a name="remarks"></a>설명

합니다 **last_is** c + + 특성에 동일한 기능을 합니다 [last_is](/windows/desktop/Midl/last-is) MIDL 특성입니다.

## <a name="example"></a>예제

참조 [first_is](first-is.md) 배열 섹션을 지정 하는 방법의 예입니다.

## <a name="requirements"></a>요구 사항

### <a name="attribute-context"></a>특성 컨텍스트

|||
|-|-|
|**적용 대상**|필드에 **구조체** 하거나 **union**인터페이스 매개 변수, 인터페이스 메서드|
|**반복 가능**|아니요|
|**필수 특성**|없음|
|**잘못된 특성**|없음|

자세한 내용은 [특성 컨텍스트](cpp-attributes-com-net.md#contexts)를 참조하세요.

## <a name="see-also"></a>참고 항목

[IDL 특성](idl-attributes.md)<br/>
[Typedef, Enum, Union 및 Struct 특성](typedef-enum-union-and-struct-attributes.md)<br/>
[매개 변수 특성](parameter-attributes.md)<br/>
[first_is](first-is.md)<br/>
[max_is](max-is.md)<br/>
[length_is](length-is.md)<br/>
[size_is](size-is.md)