---
title: 컴파일러 오류 C2702
ms.date: 11/04/2016
f1_keywords:
- C2702
helpviewer_keywords:
- C2702
ms.assetid: 6def15d4-9a8d-43e7-ae35-42d7cb57c27e
ms.openlocfilehash: 1353e16d1bfc0999a9efe7a2a3a8d80a50b41f15
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50553714"
---
# <a name="compiler-error-c2702"></a>컴파일러 오류 C2702

__except에 나타날 수 없습니다 종료 블록

예외 처리기 (`__try`/`__except`) 내에서 중첩 될 수 없습니다는 `__finally` 블록입니다.

다음 샘플에서는 C2702 오류가 생성 됩니다.

```
// C2702.cpp
// processor: x86 IPF
int Counter;
int main() {
   __try {}
   __finally {
      __try {}   // C2702
      __except( Counter ) {}   // C2702
   }
}
```