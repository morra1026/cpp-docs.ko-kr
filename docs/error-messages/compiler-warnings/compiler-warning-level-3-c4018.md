---
title: 컴파일러 경고 (수준 3) C4018 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4018
dev_langs:
- C++
helpviewer_keywords:
- C4018
ms.assetid: 6e8cbb04-d914-4319-b431-cbc2fbe40eb1
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 99ca94a47925a64c91077ad5b363e953def186b1
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46041326"
---
# <a name="compiler-warning-level-3-c4018"></a>컴파일러 경고 (수준 3) C4018

'expression': signed 또는 unsigned 일치 하지 않습니다.

컴파일러는 부호 있는 값을 부호 없는 변환할 필요 계열과 부호 없는 숫자를 비교 합니다.

부호 있는 형식과 부호 없는 테스트할 때 캐스팅 두 형식 중 하는 경우이 경고를 해결할 수 있습니다.

다음 샘플에서는 C4018 오류가 생성 됩니다.

```
// C4018.cpp
// compile with: /W3
int main() {
   unsigned int uc = 0;
   int c = 0;
   unsigned int c2 = 0;

   if (uc < c) uc = 0;   // C4018

   // OK
   if (uc == c2) uc = 0;
}
```