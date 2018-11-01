---
title: no_dual_interfaces
ms.date: 11/04/2016
f1_keywords:
- no_dual_interfaces
helpviewer_keywords:
- no_dual_interfaces attribute
ms.assetid: 9acd5d9d-4a49-4cdc-9470-73a2c23cf512
ms.openlocfilehash: d76fe3ce6bea4c3895da9d8b40d69852f912824e
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50466731"
---
# <a name="nodualinterfaces"></a>no_dual_interfaces
**C + + 전용**

컴파일러가 이중 인터페이스 메서드에 대한 래퍼 함수를 생성하는 방법을 변경합니다.

## <a name="syntax"></a>구문

```
no_dual_interfaces
```

## <a name="remarks"></a>설명

일반적으로 래퍼는 인터페이스의 가상 함수 테이블을 통해 메서드를 호출합니다. 사용 하 여 **no_dual_interfaces**, 래퍼를 대신 호출 `IDispatch::Invoke` 메서드를 호출 합니다.

**C + + 전용 종료**

## <a name="see-also"></a>참고 항목

[#import 특성](../preprocessor/hash-import-attributes-cpp.md)<br/>
[#import 지시문](../preprocessor/hash-import-directive-cpp.md)