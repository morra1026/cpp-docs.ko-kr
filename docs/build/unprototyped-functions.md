---
title: 프로토타입화되지 않은 함수
ms.date: 11/04/2016
ms.assetid: 34200b8c-5b52-4f0d-aff8-9f70d82868ed
ms.openlocfilehash: 38207be6111dadc338593e55b683b88e0480e1ca
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50633430"
---
# <a name="unprototyped-functions"></a>프로토타입화되지 않은 함수

완전히 프로토타입화 되지 않은 함수에 대 한 호출자에 게 배정밀도로 정수 및 부동 소수점 값으로 정수 값을 전달 됩니다. 부동 소수점 값을 정수 레지스터와 부동 소수점 레지스터에 모두 포함 됩니다 float 값 호출 수신자에 게 정수 레지스터의 값이 필요한 경우.

```
func1();
func2() {   // RCX = 2, RDX = XMM1 = 1.0, and R8 = 7
   func1(2, 1.0, 7);
}
```

## <a name="see-also"></a>참고 항목

[호출 규칙](../build/calling-convention.md)