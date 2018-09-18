---
title: 컴파일러 오류 C2124 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2124
dev_langs:
- C++
helpviewer_keywords:
- C2124
ms.assetid: 93392aaa-5582-4d68-8cc5-bd9c62a0ae7e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 7810565a8f7bfdac49f2c53815b9063e2e034df7
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46062323"
---
# <a name="compiler-error-c2124"></a>컴파일러 오류 C2124

0으로 나누기 또는 나머지 연산을 수행했습니다.

상수 식의 분모가 0입니다. 이 오류를 해결하려면 0으로 나누지 마세요.

다음 샘플에서는 C2124를 생성합니다.

```
// C2124.cpp
int main() {
  int i = 1 / 0;   // C2124  do not divide by zero
  int i2 = 12 / 2;   // OK
}
```