---
title: propput (c + + COM 특성)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.propput
helpviewer_keywords:
- propput attribute
ms.assetid: 1f84dda9-9cce-4e16-aaf0-b2c5219827f2
ms.openlocfilehash: 1902ba61417be457b4c296b513e1632bfdd8cec6
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50492731"
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

예를 참조 하세요 [bindable](bindable.md) 의 샘플 사용에 대 한 **propput**합니다.

## <a name="requirements"></a>요구 사항

### <a name="attribute-context"></a>특성 컨텍스트

|||
|-|-|
|**적용 대상**|메서드|
|**반복 가능**|아니요|
|**필수 특성**|없음|
|**잘못된 특성**|`propget`, `propputref`|

특성 컨텍스트에 대한 자세한 내용은 [특성 컨텍스트](cpp-attributes-com-net.md#contexts)를 참조하세요.

## <a name="see-also"></a>참고 항목

[IDL 특성](idl-attributes.md)<br/>
[메서드 특성](method-attributes.md)<br/>
[propget](propget.md)<br/>
[propputref](propputref.md)