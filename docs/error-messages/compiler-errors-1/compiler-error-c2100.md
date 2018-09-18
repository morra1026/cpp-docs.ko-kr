---
title: 컴파일러 오류 C2100 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2100
dev_langs:
- C++
helpviewer_keywords:
- C2100
ms.assetid: 9ed5ea11-9d55-4ddf-8b1a-162c74f3c390
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a663e1a433a7e2bf2ab0177a75c171aa67e12695
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46071305"
---
# <a name="compiler-error-c2100"></a>컴파일러 오류 C2100

간접 참조가 잘못 되었습니다

간접 참조 연산자 ( `*` ) 포인터가 아닌 값에 적용 됩니다.

다음 샘플에서는 C2100 오류가 생성 됩니다.

```
// C2100.cpp
int main() {
   int r = 0, *s = 0;
   s = &r;
   *r = 200;   // C2100
   *s = 200;   // OK
}
```