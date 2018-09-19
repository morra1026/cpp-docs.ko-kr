---
title: 컴파일러 경고 (수준 3) C4534 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- c4534
dev_langs:
- C++
helpviewer_keywords:
- C4534
ms.assetid: ec2adf3b-d7a1-4005-bb0c-5d219df78dc8
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ad85a6b9dff1715cbdce9738608f26c8680319d0
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46099813"
---
# <a name="compiler-warning-level-3-c4534"></a>컴파일러 경고(수준 3) C4534

'constructor'를 기본 인수 때문에 ' class' 클래스에 대 한 기본 생성자를 됩니다.

관리 되지 않는 클래스에는 기본값이 있는 매개 변수를 사용 하 여 생성자가 수 및 컴파일러가 기본 생성자로 사용 됩니다. 클래스에 표시 된 `value` 키워드는 생성자를 사용 하지는 기본값을 사용 하 여 해당 매개 변수에 대 한 기본 생성자로 합니다.

자세한 내용은 [클래스 및 구조체](../../windows/classes-and-structs-cpp-component-extensions.md)합니다.

다음 샘플에서는 C4534 오류가 생성 됩니다.

```
// C4534.cpp
// compile with: /W3 /clr /WX
value class MyClass {
public:
   int ii;
   MyClass(int i = 9) {   // C4534, will not be the default constructor
      i++;
   }
};

int main() {
   MyClass ^ xx = gcnew MyClass;
   xx->ii = 0;
}
```