---
title: 수학 오류 M6201 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- M6201
dev_langs:
- C++
helpviewer_keywords:
- M6201
ms.assetid: 4041c331-d9aa-4dd4-b565-7dbe0218538c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 87d2c09d6448bcf7fb0557fa3a174c60205a34ea
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46099397"
---
# <a name="math-error-m6201"></a>수학 오류 M6201

'function': 오류 (_d)

지정된 된 함수에 인수로 함수에 대 한 유효한 입력된 값의 도메인을 벗어났습니다.

## <a name="example"></a>예제

```
result = sqrt(-1.0)   // C statement
result = SQRT(-1.0)   !  FORTRAN statement
```

이 오류를 호출 합니다 `_matherr` 함수 이름, 해당 인수 및 오류 유형을 사용 하 여 함수입니다. 다시 작성할 수 있습니다는 `_matherr` 특정 런타임 부동 소수점 수학 오류 처리 사용자 지정 하는 함수입니다.