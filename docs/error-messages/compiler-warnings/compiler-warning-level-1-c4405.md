---
title: 컴파일러 경고 (수준 1) C4405 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4405
dev_langs:
- C++
helpviewer_keywords:
- C4405
ms.assetid: 155c64d6-58ae-4455-b61f-ccd711c5da96
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: fce005153b9343b25e7de49b3e95a002381d0619
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46061580"
---
# <a name="compiler-warning-level-1-c4405"></a>컴파일러 경고(수준 1) C4405

'identifier': 식별자가 예약어입니다.

인라인 어셈블리에 대 한 예약 된 단어를 변수 이름으로 사용 됩니다. 이 예상치 못한 결과가 발생할 수 있습니다. 이 경고를 해결 하려면 인라인 어셈블리에 대 한 예약 된 단어를 사용 하 여 변수 명명을 방지 합니다. 다음 샘플에서는 C4405 오류가 생성 됩니다.

```
// C4405.cpp
// compile with: /W1
// processor: x86
void func1() {
   int mov = 0, i = 0;
   _asm {
      mov mov, 0;   // C4405
      // instead, try ..
      // mov i, 0;
   }
}

int main() {
}
```