---
title: 컴파일러 오류 C3255
ms.date: 11/04/2016
f1_keywords:
- C3255
helpviewer_keywords:
- C3255
ms.assetid: 877ffca2-fd92-44b6-9060-6091b928b1c1
ms.openlocfilehash: a5b483f3aaa82e543d561cb7c550495069a19f7c
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50519940"
---
# <a name="compiler-error-c3255"></a>컴파일러 오류 C3255

'값 형식': 네이티브 힙에이 값 형식 개체를 동적으로 할당할 수 없습니다.

인스턴스는 값 형식 (참조 [클래스 및 구조체](../../windows/classes-and-structs-cpp-component-extensions.md)) 관리 되는 멤버를 포함 하는 힙 아니라 스택에 만들 수 있습니다.

다음 샘플에서는 C3255 오류가 생성 됩니다.

```
// C3255.cpp
// compile with: /clr
using namespace System;
value struct V {
   Object^ o;
};

value struct V2 {
   int i;
};

int main() {
   V* pv = new V;   // C3255
   V2* pv2 = new V2;
   V v2;
}
```
