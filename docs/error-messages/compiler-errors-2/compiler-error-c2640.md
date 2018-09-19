---
title: 컴파일러 오류 C2640 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2640
dev_langs:
- C++
helpviewer_keywords:
- C2640
ms.assetid: e4d137ab-ed1d-457c-9eec-b70d97f1b0b4
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ad39b2a9e3397f97ddc4a900bc45d1983ebbf574
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46085287"
---
# <a name="compiler-error-c2640"></a>컴파일러 오류 C2640

'identifier': __based 한정자를 참조

`__based` 한정자는 포인터에만 사용할 수 있습니다.

다음 샘플에서는 C2640 오류가 생성 됩니다.

```
// C2640.cpp
void f(int i) {
    void *vp;
    int _based(vp) &vr = I;  // C2640
}
```