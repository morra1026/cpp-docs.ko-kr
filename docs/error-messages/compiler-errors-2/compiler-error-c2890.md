---
title: 컴파일러 오류 C2890 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2890
dev_langs:
- C++
helpviewer_keywords:
- C2890
ms.assetid: 49147375-182c-42b1-b170-f475cd436d47
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: dbad8e1e46364579f4c7bc4bd6928e3a44d3cd66
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46042665"
---
# <a name="compiler-error-c2890"></a>컴파일러 오류 C2890

'class': ref 클래스는 하나의 비 인터페이스 기본 클래스를 하나만 사용할 수 있습니다

참조 클래스 하나의 기본 클래스를 하나만 사용할 수 있습니다.

다음 샘플에서는 C2890를 생성합니다.

```
// C2890.cpp
// compile with: /clr /c
ref class A {};
ref class B {};
ref class C : public A, public B {};   // C2890
ref class D : public A {};   // OK
```
