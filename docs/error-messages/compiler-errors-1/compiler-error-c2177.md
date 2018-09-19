---
title: 컴파일러 오류 C2177 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2177
dev_langs:
- C++
helpviewer_keywords:
- C2177
ms.assetid: 2a39a880-cddb-4d3e-a572-645a14c4c478
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 42d002b2264c9ce6b5e8d09dcda322c33b18fd05
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46096158"
---
# <a name="compiler-error-c2177"></a>컴파일러 오류 C2177

상수가 너무 큽니다.

상수 값이 할당된 변수 형식에 대해 너무 큽니다.

다음 샘플에서는 C2177을 생성합니다.

```
// C2177.cpp
int main() {
   int a=18446744073709551616;   // C2177
   int b=18446744073709551615;   // OK
}
```