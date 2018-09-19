---
title: 컴파일러 오류 C2971 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2971
dev_langs:
- C++
helpviewer_keywords:
- C2971
ms.assetid: fdb5467b-9a41-41ef-ac20-2e9428d5a4fc
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a311e6cd25ab275b7aa38325e45d26fd733d8b68
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46107541"
---
# <a name="compiler-error-c2971"></a>컴파일러 오류 C2971

'class': 템플릿 매개 변수 'param': 'arg': 지역 변수는 비형식 인수로 사용할 수 없습니다

이름 또는 지역 변수의 주소를 템플릿 인수로 사용할 수 없습니다.

다음 샘플에서는 C2971 오류가 생성 됩니다.

```
// C2971.cpp
template <int *pi>
class Y {};

int global_var = 0;

int main() {
   int local_var = 0;
   Y<&local_var> aY;   // C2971
   // try the following line instead
   // Y<&global_var> aY;
}
```