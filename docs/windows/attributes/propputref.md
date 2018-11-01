---
title: propputref (c + + COM 특성)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.propputref
helpviewer_keywords:
- propputref attribute
ms.assetid: 9b0aed74-fdc7-4e59-9117-949bea4f86dd
ms.openlocfilehash: 0ebf39be6d83e7c5a64ad29f34f9accf0743dbf4
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50551283"
---
# <a name="propputref"></a>propputref

값 대신 참조를 사용 하는 속성 설정 함수를 지정 합니다.

## <a name="syntax"></a>구문

```cpp
[propputref]
```

## <a name="remarks"></a>설명

합니다 **propputref** c + + 특성에 동일한 기능을 합니다 [propputref](/windows/desktop/Midl/propputref) MIDL 특성입니다.

## <a name="example"></a>예제

예를 참조 하세요 [bindable](bindable.md) 의 샘플 사용에 대 한 **propputref**합니다.

## <a name="requirements"></a>요구 사항

### <a name="attribute-context"></a>특성 컨텍스트

|||
|-|-|
|**적용 대상**|메서드|
|**반복 가능**|아니요|
|**필수 특성**|없음|
|**잘못된 특성**|`propget`, `propput`|

특성 컨텍스트에 대한 자세한 내용은 [특성 컨텍스트](cpp-attributes-com-net.md#contexts)를 참조하세요.

## <a name="see-also"></a>참고 항목

[IDL 특성](idl-attributes.md)<br/>
[메서드 특성](method-attributes.md)<br/>
[propget](propget.md)<br/>
[propput](propput.md)