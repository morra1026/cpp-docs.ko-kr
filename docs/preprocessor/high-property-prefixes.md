---
title: high_property_prefixes | Microsoft Docs
ms.custom: ''
ms.date: 10/18/2018
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- high_property_prefixes
dev_langs:
- C++
helpviewer_keywords:
- high_property_prefixes attribute
ms.assetid: 91c6cc2b-19b6-4aba-8831-d9e5cccb58b5
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: e3932a7632b12120e722c5f375f4387e08f1853b
ms.sourcegitcommit: 0164af5615389ffb1452ccc432eb55f6dc931047
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49809059"
---
# <a name="highpropertyprefixes"></a>high_property_prefixes

**C + + 전용**

세 가지 속성 메서드의 대체 접두사를 지정합니다.

## <a name="syntax"></a>구문

```
high_property_prefixes("GetPrefix","PutPrefix","PutRefPrefix")
```

### <a name="parameters"></a>매개 변수

*GetPrefix*<br/>
에 사용할 접두사를 `propget` 메서드.

*PutPrefix*<br/>
에 사용할 접두사를 `propput` 메서드.

*PutRefPrefix*<br/>
에 사용할 접두사를 `propputref` 메서드.

## <a name="remarks"></a>설명

기본적으로 상위 수준 오류 처리 `propget`, `propput`, 및 `propputref` 메서드는 접두사로 명명 된 멤버 함수에 의해 노출 됩니다 `Get`를 `Put`, 및 `PutRef`각각.

**C + + 전용 종료**

## <a name="see-also"></a>참고 항목

[#import 특성](../preprocessor/hash-import-attributes-cpp.md)<br/>
[#import 지시문](../preprocessor/hash-import-directive-cpp.md)