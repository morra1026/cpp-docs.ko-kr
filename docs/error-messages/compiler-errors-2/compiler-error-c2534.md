---
title: 컴파일러 오류 C2534 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2534
dev_langs:
- C++
helpviewer_keywords:
- C2534
ms.assetid: 481f9f54-5b51-4aa0-8eea-218f10807705
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 2febeeeb3b6c0e394070339f2310a22c1326ab5c
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46049035"
---
# <a name="compiler-error-c2534"></a>컴파일러 오류 C2534

'identifier': 생성자는 값을 반환할 수 없습니다.

생성자 값을 반환 하거나 반환 형식을 가질 수 없습니다 (갖추기를 `void` 반환 형식).

제거 하 여이 오류를 해결할 수 있습니다는 `return` 생성자 정의에서 문입니다.

다음 샘플에서는 C2534를 생성합니다.

```
// C2534.cpp
class A {
public:
   int i;
   A() { return i; }   // C2534
};
```