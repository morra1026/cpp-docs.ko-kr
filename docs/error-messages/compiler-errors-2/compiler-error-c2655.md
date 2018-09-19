---
title: 컴파일러 오류 C2655 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2655
dev_langs:
- C++
helpviewer_keywords:
- C2655
ms.assetid: beaefa6e-51b3-4df9-9150-960f3fbf40e0
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 456fd31e6d618774bff13c9800d6a44ffd3deb73
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46078688"
---
# <a name="compiler-error-c2655"></a>컴파일러 오류 C2655

'identifier': 정의 또는 재선언 현재 범위에서

식별자는 전역 범위 에서만 다시 선언할 수 있습니다.

다음 샘플에서는 C2655 오류가 생성 됩니다.

```
// C2655.cpp
class A {};
class B {
public:
   static int i;
};

int B::i;  // OK

int main() {
   A B::i;  // C2655
}
```