---
title: 컴파일러 경고(수준 1) C4216
ms.date: 11/04/2016
f1_keywords:
- C4216
helpviewer_keywords:
- C4216
ms.assetid: 211079dc-59d0-42a7-801c-2ddab21d7232
ms.openlocfilehash: 43c72855dbb40e93cb219e4461dbbf81d086ea79
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50650920"
---
# <a name="compiler-warning-level-1-c4216"></a>컴파일러 경고(수준 1) C4216

비표준 확장이 사용 됨: long float

기본 Microsoft 확장명 (/Ze) 취급 **long float** 으로 **double**합니다. ANSI 호환성 ([/Za](../../build/reference/za-ze-disable-language-extensions.md)) 하지 않습니다. 사용 하 여 **이중** 호환성을 유지 합니다. 다음 샘플에서는 C4216 오류가 생성 됩니다.

```
// C4216.cpp
// compile with: /W1
float long a;   // C4216

// use the line below to resolve the warning
// double a;

int main() {
}
```