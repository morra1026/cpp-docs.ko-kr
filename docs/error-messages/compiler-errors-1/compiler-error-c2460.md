---
title: 컴파일러 오류 C2460 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2460
dev_langs:
- C++
helpviewer_keywords:
- C2460
ms.assetid: d969fca9-3ac5-4e4e-88fc-df05510e2093
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: cb2d85ffbc7aa799f0688fbb10021a04ef9455ad
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46022622"
---
# <a name="compiler-error-c2460"></a>컴파일러 오류 C2460

'identifier1': 사용 하 여 'identifier2'에 정의 되는

클래스 또는 구조체 (`identifier2`)을 멤버 자체로로 선언 됩니다 (`identifier1`). 클래스 및 구조체의 재귀 정의 허용 되지 않습니다.

다음 샘플에서는 C2460 오류가 생성 됩니다.

```
// C2460.cpp
class C {
   C aC;    // C2460
};
```

대신, 클래스에 대 한 포인터 참조를 사용 합니다.

```
// C2460.cpp
class C {
   C * aC;    // OK
};
```