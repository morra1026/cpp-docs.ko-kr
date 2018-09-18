---
title: 컴파일러 오류 C2703 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2703
dev_langs:
- C++
helpviewer_keywords:
- C2703
ms.assetid: 384295c3-643d-47ae-a9a6-865b3036aa84
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 6c9f390b80179b0430e14bee3da070c0ad3b19ab
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46074737"
---
# <a name="compiler-error-c2703"></a>컴파일러 오류 C2703

잘못 된 __leave 문이

A `__leave` 문 내에 있어야 합니다.는 `__try` 블록입니다.

다음 샘플에서는 C2703를 생성합니다.

```
// C2703.cpp
int main() {
   __leave;   // C2703
   __try {
      // try the following line instead
      __leave;
   }
   __finally {}
}
```