---
title: 컴파일러 오류 C2034 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2034
dev_langs:
- C++
helpviewer_keywords:
- C2034
ms.assetid: 953d70fa-bde9-4ce6-a55d-741e7bc63ff4
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b1dadc3249b7e58410eb153f8d298fca06a44ea7
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46034423"
---
# <a name="compiler-error-c2034"></a>컴파일러 오류 C2034

'identifier': 비트 수가 너무 작아서 비트 필드의 형식

비트 필드 선언에는 비트 수가 기본 형식의 크기를 초과합니다.

다음 샘플에서는 C2034를 생성합니다.

```
// C2034.cpp
struct A {
   char test : 9;   // C2034, char has 8 bits
};
```

해결 방법:

```
// C2034b.cpp
// compile with: /c
struct A {
   char test : 8;
};
```