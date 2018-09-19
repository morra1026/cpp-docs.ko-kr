---
title: 컴파일러 오류 C2469 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2469
dev_langs:
- C++
helpviewer_keywords:
- C2469
ms.assetid: 3814bdff-581a-4d3e-8b47-8de6887cea69
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d7f9a8a8a25190163432d5f0dd7826840e7ef7c6
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46076907"
---
# <a name="compiler-error-c2469"></a>컴파일러 오류 C2469

'operator': 'type' 개체를 할당할 수 없습니다.

연산자에 잘못된 형식이 전달되었습니다.

다음 샘플에서는 C2469를 생성합니다.

```
// C2469.cpp
int main() {
   int *i = new void;   // C2469
   int *i = new int;   // OK
}
```