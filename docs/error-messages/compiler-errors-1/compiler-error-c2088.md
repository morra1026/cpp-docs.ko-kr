---
title: 컴파일러 오류 C2088 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2088
dev_langs:
- C++
helpviewer_keywords:
- C2088
ms.assetid: b93f7094-185b-423d-8bb9-507cd757dbf5
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 75281567b0e4419303607bf90a479ff628e8abf2
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46096875"
---
# <a name="compiler-error-c2088"></a>컴파일러 오류 C2088

'operator': ' s-k '에 대해 잘못 되었습니다.

연산자를 구조체 또는 공용 구조체에 대 한 정의 되지 않았습니다. 이 오류 C 코드에 대해서만 유효합니다.

다음 샘플에서는 세 번 C2088를 생성합니다.

```
// C2088.c
struct S {
   int m_i;
} s;

int main() {
   int i = s * 1;   // C2088
   struct S s2 = +s;   // C2088
   s++;   // C2088
}
```