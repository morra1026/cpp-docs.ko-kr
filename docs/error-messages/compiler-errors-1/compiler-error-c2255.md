---
title: 컴파일러 오류 C2255 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2255
dev_langs:
- C++
helpviewer_keywords:
- C2255
ms.assetid: 67dc4cb0-de6b-4405-bd64-d47736367a93
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ba6a5a2d2237373fb1321dc6d3059f20a9ddb159
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46112254"
---
# <a name="compiler-error-c2255"></a>컴파일러 오류 C2255

'element': 클래스 정의 외부에서 사용할 수 없습니다.

예를 들어 비멤버 함수를 `friend`로 선언했습니다.

다음 샘플에서는 C2255를 생성합니다.

```
// C2255.cpp
// compile with: /c
class A {
private:
   void func1();
   friend void func2();
};

friend void func1() {}   // C2255
void func2(){}
```