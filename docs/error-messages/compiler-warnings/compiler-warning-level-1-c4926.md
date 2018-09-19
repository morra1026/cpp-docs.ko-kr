---
title: 컴파일러 경고 (수준 1) C4926 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4926
dev_langs:
- C++
helpviewer_keywords:
- C4926
ms.assetid: 5717fce0-146f-4ef2-bde0-e9a01c0922d1
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 1942c334f06dce7a8f208f01cae6e2da1b6bb6cf
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46087944"
---
# <a name="compiler-warning-level-1-c4926"></a>컴파일러 경고(수준 1) C4926

'identifier': 기호를 이미 정의했으므로 특성이 무시됩니다.

정방향 선언이 있지만 이름이 같은 특성을 가진 구문이 이미 있습니다. 정방향 선언에 대한 특성은 무시됩니다.

다음 샘플에서는 C4926을 생성합니다.

```
// C4926.cpp
// compile with: /W1
[module(name="MyLib")];

[coclass]
struct a {
};

[coclass]
struct a;   // C4926

int main() {
}
```