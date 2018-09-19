---
title: 컴파일러 오류 C2267 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2267
dev_langs:
- C++
helpviewer_keywords:
- C2267
ms.assetid: ea63bebb-6208-4367-8440-39be07f9c360
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 080f6ebfda8dbdaa1f0bf70faa3b6d5c7545d66e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46035268"
---
# <a name="compiler-error-c2267"></a>컴파일러 오류 C2267

'function': 블록 범위가 있는 정적 함수는 사용할 수 없습니다.

로컬 함수를 선언 `static`합니다. 정적 함수는 전역 범위를 가져야 합니다.

다음 샘플에서는 C2267 오류가 생성 됩니다.

```
// C2267.cpp
static int func2();   // OK
int main() {
    static int func1();   // C2267
}
```