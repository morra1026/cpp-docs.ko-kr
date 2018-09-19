---
title: 컴파일러 오류 C2153 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2153
dev_langs:
- C++
helpviewer_keywords:
- C2153
ms.assetid: cfc50cb7-9a0f-4b5b-879a-d419c99f7be1
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: bbb3283ff4d27b6c939434ac3df8f8c1febf0eb3
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46051427"
---
# <a name="compiler-error-c2153"></a>컴파일러 오류 C2153

16 진 상수에는 16 진수가 적어도 하나 있어야 합니다.

16 진수 상수 0 X, x 및 \x 올바르지 않습니다. 16 진수가 적어도 하나를 수행 해야 x 또는 X입니다.

다음 샘플에서는 C2153 오류가 생성 됩니다.

```
// C2153.cpp
int main() {
   int a= 0x;    // C2153
   int b= 0xA;   // OK
}
```