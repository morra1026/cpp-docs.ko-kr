---
title: 컴파일러 오류 C2846 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2846
dev_langs:
- C++
helpviewer_keywords:
- C2846
ms.assetid: bc090ec2-5410-4112-9ec6-261325374375
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f062445aac010b5ba1ac34129590edf7b1f16932
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46067378"
---
# <a name="compiler-error-c2846"></a>컴파일러 오류 C2846

'constructor': 인터페이스는 생성자를 사용할 수 없습니다.

Visual c + + [인터페이스](../../cpp/interface.md) 생성자를 사용할 수 없습니다.

다음 샘플에서는 C2846 오류가 생성 됩니다.

```
// C2846.cpp
// compile with: /c
__interface C {
   C();   // C2846 constructor not allowed in an interface
};
```