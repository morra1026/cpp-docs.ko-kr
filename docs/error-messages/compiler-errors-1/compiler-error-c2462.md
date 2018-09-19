---
title: 컴파일러 오류 C2462 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2462
dev_langs:
- C++
helpviewer_keywords:
- C2462
ms.assetid: a8601bf8-f5ce-41de-9117-e2632bd4996b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 65df7f4fe7f3822f2723a1709751e3b9b0f23ade
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46082857"
---
# <a name="compiler-error-c2462"></a>컴파일러 오류 C2462

'identifier': ' new 식 '에서 형식을 정의할 수 없습니다

피연산자 필드의 형식을 정의할 수 없습니다는 `new` 연산자입니다. 별도 문에서 형식 정의 배치 합니다.

다음 샘플에서는 C2462 오류가 생성 됩니다.

```
// C2462.cpp
int main() {
   new struct S { int i; };   // C2462
}
```