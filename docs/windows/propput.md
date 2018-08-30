---
title: propput | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- vc-attr.propput
dev_langs:
- C++
helpviewer_keywords:
- propput attribute
ms.assetid: 1f84dda9-9cce-4e16-aaf0-b2c5219827f2
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: f6adf0f2eaf61c3a280c8ca248cffea2f05bda6f
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43213171"
---
# <a name="propput"></a>propput

속성 설정 함수를 지정합니다.

## <a name="syntax"></a>구문

```cpp
[propput]
```

## <a name="remarks"></a>설명

합니다 **propput** c + + 특성에 동일한 기능을 합니다 [propput](/windows/desktop/Midl/propput) MIDL 특성입니다.

## <a name="example"></a>예제

예를 참조 하세요 [bindable](../windows/bindable.md) 의 샘플 사용에 대 한 **propput**합니다.

## <a name="requirements"></a>요구 사항

### <a name="attribute-context"></a>특성 컨텍스트

|||
|-|-|
|**적용 대상**|메서드|
|**반복 가능**|아니요|
|**필수 특성**|없음|
|**잘못된 특성**|`propget`, `propputref`|

특성 컨텍스트에 대한 자세한 내용은 [특성 컨텍스트](../windows/attribute-contexts.md)를 참조하세요.

## <a name="see-also"></a>참고 항목

[IDL 특성](../windows/idl-attributes.md)  
[메서드 특성](../windows/method-attributes.md)  
[propget](../windows/propget.md)  
[propputref](../windows/propputref.md)