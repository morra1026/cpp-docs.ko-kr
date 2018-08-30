---
title: local (c + +) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- vc-attr.local
dev_langs:
- C++
helpviewer_keywords:
- local attribute
ms.assetid: 35cdd668-bd8e-492a-b7b8-263e7b662437
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: b910ce2416dc345e2a36c9858f260ef5b42c2cc8
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43203324"
---
# <a name="local-c"></a>local(C++)

인터페이스 헤더를 사용할 경우 MIDL 컴파일러 헤더 생성기로 사용할 수 있습니다. 개별 함수를 사용할 경우 없는 스텁 생성 되는 로컬 프로시저를 지정 합니다.

## <a name="syntax"></a>구문

```cpp
[local]
```

## <a name="remarks"></a>설명

합니다 **로컬** c + + 특성에 동일한 기능을 합니다 [로컬](/windows/desktop/Midl/local) MIDL 특성입니다.

## <a name="example"></a>예제

참조 [call_as](../windows/call-as.md) 사용 하는 방법의 예제 **로컬**합니다.

## <a name="requirements"></a>요구 사항

### <a name="attribute-context"></a>특성 컨텍스트

|||
|-|-|
|**적용 대상**|**인터페이스**, 인터페이스 메서드|
|**반복 가능**|아니요|
|**필수 특성**|없음|
|**잘못된 특성**|`dispinterface`|

자세한 내용은 [특성 컨텍스트](../windows/attribute-contexts.md)를 참조하세요.

## <a name="see-also"></a>참고 항목

[IDL 특성](../windows/idl-attributes.md)  
[인터페이스 특성](../windows/interface-attributes.md)  
[메서드 특성](../windows/method-attributes.md)  
[call_as](../windows/call-as.md)  