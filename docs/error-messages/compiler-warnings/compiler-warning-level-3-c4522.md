---
title: 컴파일러 경고 (수준 3) C4522 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4522
dev_langs:
- C++
helpviewer_keywords:
- C4522
ms.assetid: 7065dc27-0b6c-4e68-a345-c51cdb99a20b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 65662d3e62abbeb06127c7b5a49479a23fb20a7a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46070940"
---
# <a name="compiler-warning-level-3-c4522"></a>컴파일러 경고(수준 3) C4522

'class': 할당 연산자가 여러 개 지정

클래스에는 단일 형식의 여러 할당 연산자가 있습니다. 이 경고는 정보를 제공 합니다. 생성자는 프로그램에서 호출할 수 있습니다.

사용 합니다 [경고](../../preprocessor/warning.md) pragma를이 경고를 표시 합니다.

## <a name="example"></a>예제

다음 샘플에서는 C4522 오류가 발생 합니다.

```
// C4522.cpp
// compile with: /EHsc /W3
#include <iostream>

using namespace std;
class A {
public:
   A& operator=( A & o ) { cout << "A&" << endl; return *this; }
   A& operator=( const A &co ) { cout << "const A&" << endl; return *this; }   // C4522
};

int main() {
   A o1, o2;
   o2 = o1;
   const A o3;
   o1 = o3;
}
```