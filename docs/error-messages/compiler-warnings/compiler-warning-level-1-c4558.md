---
title: 컴파일러 경고 (수준 1) C4558 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4558
dev_langs:
- C++
helpviewer_keywords:
- C4558
ms.assetid: 52bb0324-7bec-468c-b35b-13a08d38e578
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 404f4a343b35081a64267424c436063c085958e7
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46056653"
---
# <a name="compiler-warning-level-1-c4558"></a>컴파일러 경고(수준 1) C4558

'value' 피연산자의 값 'lowerbound-자체도' 범위를 벗어났습니다.

어셈블리 언어 명령에 전달 되는 값 매개 변수에 대해 지정 된 범위를 벗어났습니다. 값은 잘립니다.

다음 샘플에서는 C4558 오류가 생성 됩니다.

```
// C4558.cpp
// compile with: /W1
// processor: x86
void asm_test() {
   __asm pinsrw   mm1, eax, 8;   // C4558
}

int main() {
}
```