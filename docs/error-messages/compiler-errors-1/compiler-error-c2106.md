---
title: 컴파일러 오류 C2106 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2106
dev_langs:
- C++
helpviewer_keywords:
- C2106
ms.assetid: d5c91a2e-04e4-4770-8478-788b98c52a53
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 68dd34810041b9d71056d4bb4afc9beadcaffa81
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46030744"
---
# <a name="compiler-error-c2106"></a>컴파일러 오류 C2106

'operator': 왼쪽된 피연산자 l 값 이어야 합니다.

연산자 왼쪽 피연산자로 l-value가 있어야 합니다.

다음 샘플에서는 C2106 오류가 생성 됩니다.

```
// C2106.cpp
int main() {
   int a;
   1 = a;   // C2106
   a = 1;   // OK
}
```