---
title: 컴파일러 오류 C2087 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2087
dev_langs:
- C++
helpviewer_keywords:
- C2087
ms.assetid: 89761e83-415a-4468-a4c6-b6dedfd1dd6a
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 38b6ce6c0b2435143ece8d431271c97a3f48a2b2
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46101958"
---
# <a name="compiler-error-c2087"></a>컴파일러 오류 C2087

'identifier': 첨자가 없습니다

여러 첨자가 포함 된 배열을 정의 1 보다 더 높은 차원의 첨자 값이 없습니다.

다음 샘플에서는 C2087 오류가 생성 됩니다.

```
// C2087.cpp
int main() {
   char a[10][];   // C2087
}
```

해결 방법:

```
// C2087b.cpp
int main() {
   char b[4][5];
}
```