---
title: 컴파일러 오류 C2273 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2273
dev_langs:
- C++
helpviewer_keywords:
- C2273
ms.assetid: 3c682c66-97bf-4a23-a22c-d9a26a92bf95
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 995f75487820976d045e5db05fe2b170260240cc
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46066221"
---
# <a name="compiler-error-c2273"></a>컴파일러 오류 C2273

'type': '->' 연산자의 오른쪽에 사용할 수 없습니다.

오른쪽 피연산자로 형식이 표시를 `->` 연산자입니다.

이 오류는 사용자 정의 형식 변환에 액세스 하려고 시도 하 여 발생할 수 있습니다. ->와 `operator` 사이에 `type` 키워드를 사용하십시오.

다음 샘플에서는 C2273를 생성합니다.

```
// C2273.cpp
struct MyClass {
   operator int() {
      return 0;
   }
};
int main() {
   MyClass * ClassPtr = new MyClass;
   int i = ClassPtr->int();   // C2273
   int j = ClassPtr-> operator int();   // OK
}
```