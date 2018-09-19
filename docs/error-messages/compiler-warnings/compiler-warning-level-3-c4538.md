---
title: 컴파일러 경고 (수준 3) C4538 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4538
dev_langs:
- C++
helpviewer_keywords:
- C4538
ms.assetid: 747e3d51-b6d0-41c1-a726-7af3253b59d7
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 5c4d9095eef3e37aaa487ebec9ae271bcd48c74f
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46075529"
---
# <a name="compiler-warning-level-3-c4538"></a>컴파일러 경고(수준 3) C4538

'type':이 형식에서 const/volatile 한정자는 지원 되지 않습니다

한정자 키워드 올바르게 적용 되었습니다를 배열 합니다. 자세한 내용은 [배열](../../windows/arrays-cpp-component-extensions.md)을 참조하세요.

다음 샘플에서는 C4538 오류가 생성 됩니다.

```
// C4538.cpp
// compile with: /clr /W3 /LD
const array<int> ^f1();   // C4538
array<const int> ^f2();   // OK
```