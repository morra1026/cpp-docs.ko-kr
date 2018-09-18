---
title: 컴파일러 경고 (수준 3) C4265 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4265
dev_langs:
- C++
helpviewer_keywords:
- C4265
ms.assetid: 20547159-6f30-4cc4-83aa-927884c8bb4c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 0df54714038ab0fb6020e34aa35d677af5e899b4
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46016132"
---
# <a name="compiler-warning-level-3-c4265"></a>컴파일러 경고(수준 3) C4265

'class': 클래스에 가상 함수가 있지만 소멸자는 가상이 아닙니다

클래스에 가상 함수가 있지만 비가상 소멸자가 있는 경우 형식의 개체 클래스는 기본 클래스 포인터를 통해 소멸 될 때 제대로 소멸 되지 않습니다.

기본적으로 이 경고는 해제되어 있습니다. 자세한 내용은 [기본적으로 해제되어 있는 컴파일러 경고](../../preprocessor/compiler-warnings-that-are-off-by-default.md) 를 참조하세요.

다음 샘플에서는 C4265 오류가 생성 됩니다.

```
// C4265.cpp
// compile with: /W3 /c
#pragma warning(default : 4265)
class B
{
public:
   virtual void vmf();

   ~B();
   // try the following line instead
   // virtual ~B();
};   // C4265

int main()
{
   B b;
}
```