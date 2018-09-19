---
title: 컴파일러 오류 C2007 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2007
dev_langs:
- C++
helpviewer_keywords:
- C2007
ms.assetid: ecd09d99-5036-408b-9e46-bc15488f049e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d2ac9383b144496228038529808e24dfd1c0f7a1
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46097330"
---
# <a name="compiler-error-c2007"></a>컴파일러 오류 C2007

\#구문 정의

식별자가 없는 뒤를 `#define`입니다. 이 오류를 해결 하려면 식별자를 사용 합니다.

다음 샘플에서는 C2007 오류가 생성 됩니다.

```
// C2007.cpp
#define   // C2007
```

해결 방법:

```
// C2007b.cpp
// compile with: /c
#define true 1
```