---
title: 컴파일러 오류 C3697 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3697
dev_langs:
- C++
helpviewer_keywords:
- C3697
ms.assetid: 2d3f63c4-b7f8-421d-a7a5-2bf17fd054f9
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 6cb5755cc737c0cc5524cb6abd980b70d08b6cf8
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46050660"
---
# <a name="compiler-error-c3697"></a>컴파일러 오류 C3697

'한정자':이 한정자를 사용할 수 없습니다 ' ^'

추적 핸들 (^)에 사용할 수 없는 한정자를 적용 했습니다.

다음 샘플에서는 C3697 오류가 생성 됩니다.

```
// C3697.cpp
// compile with: /clr
using namespace System;
int main() {
   String ^__restrict s;   // C3697
   String ^ s2;   // OK
}
```