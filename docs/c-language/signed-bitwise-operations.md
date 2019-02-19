---
title: 부호 있는 비트 연산
ms.date: 11/04/2016
helpviewer_keywords:
- bitwise operations
- signed bitwise operations
ms.assetid: 1e5cf65b-ee32-41a0-a5c2-82c1854091f6
ms.openlocfilehash: 43f65fd5d1ea14ef5e15f18d9c8516ccf5fb1e08
ms.sourcegitcommit: f4be868c0d1d78e550fba105d4d3c993743a1f4b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56147596"
---
# <a name="signed-bitwise-operations"></a>부호 있는 비트 연산

**ANSI 3.3** 부호 있는 정수에 대한 비트 연산의 결과

부호 있는 정수에 대한 비트 연산은 부호 없는 정수에 대한 비트 연산과 동일하게 작동합니다. 예를 들어, `-16 & 99`는 이진 형식으로 다음과 같이 표현될 수 있습니다.

```
  11111111 11110000
& 00000000 01100011
  _________________
  00000000 01100000
```

비트 AND의 결과는 96입니다.

## <a name="see-also"></a>참고 항목

[정수](../c-language/integers.md)
