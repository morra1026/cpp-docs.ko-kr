---
title: 컴파일러 오류 C2702 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2702
dev_langs:
- C++
helpviewer_keywords:
- C2702
ms.assetid: 6def15d4-9a8d-43e7-ae35-42d7cb57c27e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: cbec8fe50c87cfc609cad5098779bc22ddae84cb
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46061241"
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