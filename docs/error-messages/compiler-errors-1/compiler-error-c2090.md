---
title: 컴파일러 오류 C2090 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2090
dev_langs:
- C++
helpviewer_keywords:
- C2090
ms.assetid: e8176e55-382b-453d-aa27-6597f0274afd
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 613d3214e652e994ec07e1fe4396b4eb15798067
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46028781"
---
# <a name="compiler-error-c2090"></a>컴파일러 오류 C2090

함수가 배열을 반환합니다.

함수는 배열을 반환할 수 없습니다. 대신 배열에 대 한 포인터를 반환 합니다.

다음 샘플에서는 C2090 오류가 생성 됩니다.

```
// C2090.cpp
int func1(void)[] {}   // C2090
```

해결 방법:

```
// C2090b.cpp
// compile with: /c
int* func2(int * i) {
   return i;
}
```