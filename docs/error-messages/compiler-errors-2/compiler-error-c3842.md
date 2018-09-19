---
title: 컴파일러 오류 C3842 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3842
dev_langs:
- C++
helpviewer_keywords:
- C3842
ms.assetid: 41a1a44a-c618-40a2-8d26-7da27d14095d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 8db69ce3af28ed5878c43775b2c33542e5c817d6
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46055528"
---
# <a name="compiler-error-c3842"></a>컴파일러 오류 C3842

'function': WinRT 또는 관리되는 형식의 멤버 함수에 'const' 및 'volatile' 한정자를 사용할 수 없습니다.

[const](../../cpp/const-cpp.md) 하 고 [volatile](../../cpp/volatile-cpp.md) Windows 런타임 또는 관리 되는 형식의 멤버 함수에서 지원 되지 않습니다.

다음 샘플에서는 C3842를 생성합니다.

```
// C3842a.cpp
// compile with: /clr /c
public ref struct A {
   void f() const {}   // C3842
   void f() volatile {}   // C3842

   void f() {}
};
```