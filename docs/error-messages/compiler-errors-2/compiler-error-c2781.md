---
title: 컴파일러 오류 C2781 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2781
dev_langs:
- C++
helpviewer_keywords:
- C2781
ms.assetid: f29b9963-f55b-427c-8db6-50f37713df5a
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 3662a1be167f6a443606139ff49daebc5c923eec
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46095484"
---
# <a name="compiler-error-c2781"></a>컴파일러 오류 C2781

'declaration': 적어도 value1 인수-value2 제공

가변 매개 변수 목록 사용 하 여 함수 템플릿 인수가 너무 적습니다.

다음 샘플에서는 C2781 오류가 생성 됩니다.

```
// C2781.cpp
template<typename T>
void f(T, T, ...){}

int main() {
   f(1);   // C2781

   // try the following line instead
   f(1,1);
}
```