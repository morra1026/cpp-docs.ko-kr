---
title: helpfile | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- vc-attr.helpfile
dev_langs:
- C++
helpviewer_keywords:
- helpfile attribute
ms.assetid: d75161c1-1363-4019-ae09-e7e3b8a3971e
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 66cd89c28ea01c3a75d0cb25aa6f96a234e379b2
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46418205"
---
# <a name="helpfile"></a>helpfile

형식 라이브러리에 대 한 도움말 파일의 이름을 설정합니다.

## <a name="syntax"></a>구문

```cpp
[ helpfile(
   "filename"
) ]
```

### <a name="parameters"></a>매개 변수

*filename*<br/>
도움말 항목이 포함 된 파일의 이름입니다.

## <a name="remarks"></a>설명

합니다 **helpfile** c + + 특성에 동일한 기능을 합니다 [helpfile](/windows/desktop/Midl/helpfile) MIDL 특성입니다.

## <a name="example"></a>예제

예를 참조 하세요 [모듈](../windows/module-cpp.md) 사용 하는 방법의 예제 **helpfile**합니다.

## <a name="requirements"></a>요구 사항

### <a name="attribute-context"></a>특성 컨텍스트

|||
|-|-|
|**적용 대상**|**인터페이스**, **typedef**합니다 **클래스**, 메서드, **속성**|
|**반복 가능**|아니요|
|**필수 특성**|없음|
|**잘못된 특성**|없음|

자세한 내용은 [특성 컨텍스트](../windows/attribute-contexts.md)를 참조하세요.

## <a name="see-also"></a>참고 항목

[IDL 특성](../windows/idl-attributes.md)<br/>
[인터페이스 특성](../windows/interface-attributes.md)<br/>
[클래스 특성](../windows/class-attributes.md)<br/>
[메서드 특성](../windows/method-attributes.md)<br/>
[Typedef, Enum, Union 및 Struct 특성](../windows/typedef-enum-union-and-struct-attributes.md)<br/>
[helpcontext](../windows/helpcontext.md)<br/>
[helpstring](../windows/helpstring.md)  