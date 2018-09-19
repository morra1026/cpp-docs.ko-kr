---
title: 컴파일러 오류 C2831 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2831
dev_langs:
- C++
helpviewer_keywords:
- C2831
ms.assetid: c8c04288-0889-4265-a077-17f94cbcdcc9
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a534fd379e8ec250f185370d7388171dc9ef3508
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46047592"
---
# <a name="compiler-error-c2831"></a>컴파일러 오류 C2831

'operator o'는 기본 매개 변수를 사용할 수 없습니다.

세 명의 연산자는 기본 매개 변수를 포함할 수 있습니다.

- [new](../../cpp/new-operator-cpp.md)

- 할당 =

- 왼쪽된 괄호 (

다음 샘플에서는 C2831 오류가 생성 됩니다.

```
// C2831.cpp
// compile with: /c
#define BINOP <=
class A {
public:
   int i;
   int operator BINOP(int x = 1) {   // C2831
   // try the following line instead
   // int operator BINOP(int x) {
      return i+x;
   }
};
```