---
title: 컴파일러 경고 (수준 2) C4307 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4307
dev_langs:
- C++
helpviewer_keywords:
- C4307
ms.assetid: 7cca11e9-be61-49e4-8b15-88b84f0cbf07
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ed18c213b35e79aaae98efa5932ac404a8d84bff
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46079195"
---
# <a name="compiler-warning-level-2-c4307"></a>컴파일러 경고(수준 2) C4307

'operator': 정수 계열 상수가 오버플로 됩니다.

연산자는 정수 상수에 할당 된 공간에 오버플로가 발생 하는 식에 사용 됩니다. 상수에 대 한 더 큰 형식을 사용 해야 합니다. **int 서명** 보다 작은 값을 저장를 `unsigned int` 때문에 **int 서명** 부호를 나타내는 1 비트를 사용 합니다.

다음 샘플에서는 C4307 오류가 생성 됩니다.

```
// C4307.cpp
// compile with: /W2
int i = 2000000000 + 2000000000;   // C4307
int j = (unsigned)2000000000 + 2000000000;   // OK

int main()
{
}
```