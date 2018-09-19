---
title: 컴파일러 경고 (수준 4) C4516 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4516
dev_langs:
- C++
helpviewer_keywords:
- C4516
ms.assetid: 6677bb1f-d26e-4ab9-8644-6b5a2a8f4ff8
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 88bb2232c635a89650be892a27e490a42d7197ca
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46045627"
---
# <a name="compiler-warning-level-4-c4516"></a>컴파일러 경고(수준 4) C4516

'class::symbol': 액세스 선언은 사용 되지 않습니다. 더 나은 대안을 제공 하는 멤버를 사용 하 여 선언

ANSI c + + 위원회에 대 한 액세스 선언이 했습니다 (하지 않고 파생된 클래스에서 멤버의 액세스를 변경 합니다 [를 사용 하 여](../../cpp/using-declaration.md) 키워드) 오래 된 되도록 합니다. 액세스 선언은 c + +의 이후 버전에서 지원 되지 않을 수 있습니다.

다음 샘플에서는 C4516 오류가 생성 됩니다.

```
// C4516.cpp
// compile with: /W4
class A
{
public:
   void x(char);
};

class B : protected A
{
public:
   A::x;  // C4516 on access-declaration
   // use the following line instead
   // using A::x; // using-declaration, ok
};

int main()
{
}
```