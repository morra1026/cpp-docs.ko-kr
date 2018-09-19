---
title: 컴파일러 오류 C2149 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2149
dev_langs:
- C++
helpviewer_keywords:
- C2149
ms.assetid: 7a106dab-d79f-41b9-85be-f36e86e4d2ab
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 38ebb710cc9f4d5f546c40d84909dbe23805f2f7
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46094925"
---
# <a name="compiler-error-c2149"></a>컴파일러 오류 C2149

'identifier': 명명된 비트 필드의 너비가 0일 수 없습니다.

비트 필드는 명명되지 않은 경우에만 너비가 0일 수 있습니다.

다음 샘플에서는 C2149를 생성합니다.

```
// C2149.cpp
// compile with: /c
struct C {
   int i : 0;   // C2149
   int j : 2;   // OK
};
```