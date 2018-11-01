---
title: 컴파일러 오류 C2800
ms.date: 11/04/2016
f1_keywords:
- C2800
helpviewer_keywords:
- C2800
ms.assetid: a2f1a590-9fe6-44cb-ad09-b4505ef47c6a
ms.openlocfilehash: e893866a28c124e9e6cbc9663a488f89ac2d291b
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50516898"
---
# <a name="compiler-error-c2800"></a>컴파일러 오류 C2800

'operator o'를 오버 로드할 수 없습니다.

다음 연산자를 오버 로드할 수 없습니다: 클래스 멤버 액세스 (`.`), 멤버 포인터 (`.*`), 범위 결정 (`::`), 조건식 (`? :`), 및 `sizeof`합니다.

다음 샘플에서는 C2800 오류가 생성 됩니다.

```
// C2800.cpp
// compile with: /c
class C {
   operator:: ();   // C2800
};
```