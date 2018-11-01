---
title: 컴파일러 오류 C2850
ms.date: 11/04/2016
f1_keywords:
- C2850
helpviewer_keywords:
- C2850
ms.assetid: f3efe86c-4168-4e76-a133-3f8314c69f51
ms.openlocfilehash: 34c2054226ea452f76fdb15b87454677a6a6fe8e
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50611772"
---
# <a name="compiler-error-c2850"></a>컴파일러 오류 C2850

'construct': 파일 범위에만 추가할 수 중첩된 된 구문에 사용할 수 없습니다.

일부 pragma 등과 같은 구문을 전역 범위에만 나타날 수 있습니다.

다음 샘플에서는 C2850 오류가 생성 됩니다.

```
// C2850.cpp
// compile with: /c /Yc
// try the following line instead
// #pragma hdrstop
namespace X {
   #pragma hdrstop   // C2850
};
```