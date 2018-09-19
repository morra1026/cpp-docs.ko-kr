---
title: 컴파일러 오류 C3736 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3736
dev_langs:
- C++
helpviewer_keywords:
- C3736
ms.assetid: 579b773c-41e7-40ea-8382-2e3ce2667f4c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f0a98d1e34a7dbf9e951649d88cd5a96d9f12a8a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46069029"
---
# <a name="compiler-error-c3736"></a>컴파일러 오류 C3736

'event': 메서드 이거나, 관리 되는 이벤트의 경우 데이터 멤버

네이티브 및 COM 이벤트에는 메서드가 있어야 합니다. .NET 이벤트 데이터 멤버를 수도 있습니다.

다음 샘플에서는 C3736 오류가 생성 됩니다.

```
// C3736.cpp
struct A {
   __event int e();
};

struct B {
   int f;   // C3736
   // The following line resolves the error.
   // int f();
   B(A* a) {
      __hook(&A::e, a, &B::f);
   }
};

int main() {
}
```