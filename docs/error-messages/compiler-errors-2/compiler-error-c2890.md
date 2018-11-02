---
title: 컴파일러 오류 C2890
ms.date: 11/04/2016
f1_keywords:
- C2890
helpviewer_keywords:
- C2890
ms.assetid: 49147375-182c-42b1-b170-f475cd436d47
ms.openlocfilehash: 43c05fba15ee78c8e1454c115246f557f98f897e
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50661476"
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
