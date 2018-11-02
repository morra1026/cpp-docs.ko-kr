---
title: 컴파일러 오류 C2279
ms.date: 11/04/2016
f1_keywords:
- C2279
helpviewer_keywords:
- C2279
ms.assetid: 1b5c88ef-2336-49b8-9ddb-d61f97c73e14
ms.openlocfilehash: f35e384a5b242eb28427e1ff62ac55a3e9b206c4
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50666224"
---
# <a name="compiler-error-c2279"></a>컴파일러 오류 C2279

typedef 선언에 예외 사양이 나타날 수 없습니다.

아래 **/Za**를 [예외 사양](../../cpp/exception-specifications-throw-cpp.md) typedef 선언은 허용 되지 않습니다.

다음 샘플에서는 C2279를 생성합니다.

```
// C2279.cpp
// compile with: /Za /c
typedef int (*xy)() throw(...);   // C2279
typedef int (*xyz)();   // OK
```