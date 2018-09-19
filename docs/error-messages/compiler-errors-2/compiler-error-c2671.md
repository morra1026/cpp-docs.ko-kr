---
title: 컴파일러 오류 C2671 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2671
dev_langs:
- C++
helpviewer_keywords:
- C2671
ms.assetid: fc0ee40f-c8f3-408f-b89d-745d149c4169
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b37d9dc1e50da921bdbe758e73257100853517eb
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46026161"
---
# <a name="compiler-error-c2671"></a>컴파일러 오류 C2671

'function': 정적 멤버 함수에 'this' 포인터가 없습니다.

A `static` 멤버 함수에 액세스 하려고 `this`합니다.

다음 샘플에서는 C2671 오류가 생성 됩니다.

```
// C2671.cpp
struct S {
   static S* const func() { return this; }  // C2671
};
```