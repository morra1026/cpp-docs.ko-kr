---
title: 컴파일러 오류 C2137 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2137
dev_langs:
- C++
helpviewer_keywords:
- C2137
ms.assetid: 984687ee-7766-4f6b-ae15-0c9a010e2366
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 11351f62664d2404bef1217c2f0815b1047964ab
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46036828"
---
# <a name="compiler-error-c2137"></a>컴파일러 오류 C2137

문자 상수가 비어 있습니다.

빈 문자 상수(' ')는 허용되지 않습니다.

다음 샘플에서는 C2137을 생성합니다.

```
// C2137.cpp
int main() {
   char c = '';   // C2137
   char d = ' ';   // OK
}
```