---
title: helpcontext | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- vc-attr.helpcontext
dev_langs:
- C++
helpviewer_keywords:
- helpcontext attribute
ms.assetid: 6fbb022d-a4b7-4989-a02f-7f18a9b0ad96
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 5644f99e15685f8f1784cc40886709b05a9a06bd
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43221286"
---
# <a name="helpcontext"></a>helpcontext

이 요소에 대 한 정보를 볼 수 있는 컨텍스트 ID를 지정 합니다 **도움말** 파일입니다.

## <a name="syntax"></a>구문

```cpp
[ helpcontext(
   id
) ]
```

### <a name="parameters"></a>매개 변수

*ID*  
도움말 항목의 컨텍스트 ID입니다. 참조 [HTML 도움말: 프로그램에 대 한 상황에 맞는 도움말](../mfc/html-help-context-sensitive-help-for-your-programs.md) 컨텍스트 Id에 대 한 자세한 내용은 합니다.

## <a name="remarks"></a>설명

합니다 **helpcontext** c + + 특성에 동일한 기능을 합니다 [helpcontext](/windows/desktop/Midl/helpcontext) MIDL 특성입니다.

## <a name="example"></a>예제

예를 참조 하세요 [defaultvalue](../windows/defaultvalue.md) 사용 하는 방법의 예제 **helpcontext**합니다.

## <a name="requirements"></a>요구 사항

### <a name="attribute-context"></a>특성 컨텍스트

|||
|-|-|
|**적용 대상**|**인터페이스**하십시오 **typedef**를 **클래스**, 메서드, 속성|
|**반복 가능**|아니요|
|**필수 특성**|없음|
|**잘못된 특성**|없음|

자세한 내용은 [특성 컨텍스트](../windows/attribute-contexts.md)를 참조하세요.

## <a name="see-also"></a>참고 항목

[IDL 특성](../windows/idl-attributes.md)  
[인터페이스 특성](../windows/interface-attributes.md)  
[클래스 특성](../windows/class-attributes.md)  
[메서드 특성](../windows/method-attributes.md)  
[Typedef, Enum, Union 및 Struct 특성](../windows/typedef-enum-union-and-struct-attributes.md)  
[helpfile](../windows/helpfile.md)  
[helpstring](../windows/helpstring.md)  