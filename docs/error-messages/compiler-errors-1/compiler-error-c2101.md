---
title: 컴파일러 오류 C2101 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2101
dev_langs:
- C++
helpviewer_keywords:
- C2101
ms.assetid: 42f0136f-8cc1-4f2b-be1c-721ec9278e66
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 247bd168e1ea82d4533c794ae5c14d34a49064d0
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46041365"
---
# <a name="compiler-error-c2101"></a>컴파일러 오류 C2101

상수에 '&'가 있습니다.

연산자 주소( `&` )에 피연산자로 l 값이 있어야 합니다.

다음 샘플에서는 C2101을 생성합니다.

```
// C2101.cpp
int main() {
   char test;
   test = &'a';   // C2101
   test = 'a';   // OK
}
```