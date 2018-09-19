---
title: 컴파일러 경고 (수준 4) C4740 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4740
dev_langs:
- C++
helpviewer_keywords:
- C4740
ms.assetid: 85528969-966a-44b4-8a2f-971704c64477
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 6353ac464d95e8805a9c9e55488a355f71372508
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46056159"
---
# <a name="compiler-warning-level-4-c4740"></a>컴파일러 경고(수준 4) C4740

인라인 asm 코드 안팎에서 흐름을 선택 하면 전역 최적화

부재 중 또는 점프 경우는 `asm` 블록에 해당 함수에 대 한 전역 최적화가 해제 됩니다.

다음 샘플에서는 C4740 오류가 생성 됩니다.

```
// C4740.cpp
// compile with: /O2 /W4
// processor: x86
int main() {
   __asm jmp tester
   tester:;
}
```