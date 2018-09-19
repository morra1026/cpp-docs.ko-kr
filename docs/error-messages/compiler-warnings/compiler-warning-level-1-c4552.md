---
title: 컴파일러 경고 (수준 1) C4552 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4552
dev_langs:
- C++
helpviewer_keywords:
- C4552
ms.assetid: ebbbb5ee-1c19-45bd-b386-41a19630fc76
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 62c08ea81f5f8794a1dd4ff7d0b5644e9a669e0f
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46048073"
---
# <a name="compiler-warning-level-1-c4552"></a>컴파일러 경고(수준 1) C4552

'operator': 연산자에 영향을 주지 않습니다. 파생 작업이 있는 연산자 여야 합니다.

식 문의 top 식의 부작용 없음 연산자 있으면 실수 때문일 수 있습니다.

이 경고를 무시 하려면 식을 괄호로 배치 합니다.

다음 샘플에서는 C4552 오류가 생성 됩니다.

```
// C4552.cpp
// compile with: /W1
int main() {
   int i, j;
   i + j;   // C4552
   // try the following line instead
   // (i + j);
}
```