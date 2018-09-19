---
title: 컴파일러 오류 C3182 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3182
dev_langs:
- C++
helpviewer_keywords:
- C3182
ms.assetid: f3681266-308e-4990-a979-8eef8920e186
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 722f95b41f9f5ec467af25ccf927631590f90e45
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46110222"
---
# <a name="compiler-error-c3182"></a>컴파일러 오류 C3182

'class': using 선언 또는 액세스 선언 멤버를 관리 되는 또는 WinRTtype 내에서 유효 하지 않은

A [를 사용 하 여](../../cpp/using-declaration.md) 선언은 모든 형식의 관리 되는 클래스 내에서 올바르지 않습니다.

다음 샘플에서는 C3182 오류가 발생하는 경우 및 이를 해결하는 방법을 보여 줍니다.

```
// C3182a.cpp
// compile with: /clr /c
ref struct B {
   void mf(int) {
   }
};

ref struct D : B {
   using B::mf;   // C3182, delete to resolve
   void mf(char) {
   }
};
```
