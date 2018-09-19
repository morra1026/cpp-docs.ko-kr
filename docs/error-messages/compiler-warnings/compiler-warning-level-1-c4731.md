---
title: 컴파일러 경고 (수준 1) C4731 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4731
dev_langs:
- C++
helpviewer_keywords:
- C4731
ms.assetid: 5658c24c-3e6f-4505-835b-1fb92d47cab0
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 75117b34e63694cfa6aeec97abf178ff8e61a7da
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46086488"
---
# <a name="compiler-warning-level-1-c4731"></a>컴파일러 경고(수준 1) C4731

'pointer': 프레임 포인터 레지스터가 인라인 어셈블리 코드에 의해 수정 '등록'

프레임 포인터 레지스터를 수정 했습니다. 저장 하 고를 인라인 어셈블리 블록 또는 프레임 변수 (로컬 또는 매개 변수를 수정 하는 레지스터에 따라) 레지스터를 복원 해야 하거나 코드가 제대로 작동 하지 않을 수 있습니다.

다음 샘플에서는 C4731 오류가 생성 됩니다.

```
// C4731.cpp
// compile with: /W1 /LD
// processor: x86
// C4731 expected
void bad(int p) {
   __asm
   {
      mov ebp, 1
   }

   if (p == 1)
   {
      // ...
   }
}
```

EBP 프레임 포인터 (fpo 거부 됨) 이며 수정 중입니다. 때 `p` 중이면 적절 하 게 참조는 참조 `EBP`합니다. 하지만 `EBP` 코드 되므로 프로그램이 제대로 작동 하지 것입니다 오류도 덮어 쓰여졌습니다.