---
title: 컴파일러 경고(수준 4) C4515
ms.date: 11/04/2016
f1_keywords:
- C4515
helpviewer_keywords:
- C4515
ms.assetid: 167b5177-3f89-418b-b6c8-7de634f6b28f
ms.openlocfilehash: 147855f607d8ca72aa32548bf817484b6c0c3cfe
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50459659"
---
# <a name="compiler-warning-level-4-c4515"></a>컴파일러 경고(수준 4) C4515

'namespace': 자체 네임 스페이스 사용

네임 스페이스를 재귀적으로 사용된 합니다.

다음 샘플에서는 C4515 오류가 생성 됩니다.

```
// C4515.cpp
// compile with: /W4
namespace A
{
   using namespace A; // C4515
}

int main()
{
}
```