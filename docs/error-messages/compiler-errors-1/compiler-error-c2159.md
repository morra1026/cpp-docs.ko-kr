---
title: 컴파일러 오류 C2159 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2159
dev_langs:
- C++
helpviewer_keywords:
- C2159
ms.assetid: 925a2cbd-43c9-45ee-a373-84004350b380
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 3c33f8faebbca2999a893ceb1d0650ba89ee74bf
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46048489"
---
# <a name="compiler-error-c2159"></a>컴파일러 오류 C2159

저장소 클래스를 두 개 이상 지정했습니다.

선언에 저장소 클래스가 둘 이상 포함되어 있습니다.

다음 샘플에서는 C2159를 생성합니다.

```
// C2159.cpp
// compile with: /c
static int i;   // OK
extern static int i;   // C2159
```