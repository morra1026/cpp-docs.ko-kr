---
title: 컴파일러 오류 C2459 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2459
dev_langs:
- C++
helpviewer_keywords:
- C2459
ms.assetid: 81e29f4c-5b60-40fb-9557-1cdc630d77e8
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 0b67c5ba4c714b096da58b1e4d837840dc6b5fd2
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46113216"
---
# <a name="compiler-error-c2459"></a>컴파일러 오류 C2459

'identifier': 정의 하 고 있습니다. 익명 멤버로 서 추가할 수 없습니다.

클래스, 구조체 또는 공용 구조체는 자체 범위에서 익명 공용 구조체의 멤버에 의해 재정의 됩니다.

다음 샘플에서는 C2459 오류가 생성 됩니다.

```
// C2459.cpp
// compile with: /c
class C {
   union { int C; };   // C2459
   union { int D; };
};
```