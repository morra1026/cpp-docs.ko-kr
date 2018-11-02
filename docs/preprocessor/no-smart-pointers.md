---
title: no_smart_pointers
ms.date: 11/04/2016
f1_keywords:
- no_search_pointers
helpviewer_keywords:
- no_smart_pointers attribute
ms.assetid: d69dd71e-08a8-4446-a3d0-a062dc29cb17
ms.openlocfilehash: 305c08497a600f602767496cba48d108335fdeb8
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50636984"
---
# <a name="nosmartpointers"></a>no_smart_pointers
**C + + 전용**

형식 라이브러리의 모든 인터페이스에 대한 스마트 포인터를 만들지 않습니다.

## <a name="syntax"></a>구문

```
no_smart_pointers
```

## <a name="remarks"></a>설명

`#import`를 사용하는 경우 기본적으로 형식 라이브러리에 있는 모든 인터페이스에 대한 스마트 포인터 선언을 가져옵니다. 이러한 스마트 포인터는 형식이 [_com_ptr_t 클래스](../cpp/com-ptr-t-class.md)합니다.

**C + + 전용 종료**

## <a name="see-also"></a>참고 항목

[#import 특성](../preprocessor/hash-import-attributes-cpp.md)<br/>
[#import 지시문](../preprocessor/hash-import-directive-cpp.md)