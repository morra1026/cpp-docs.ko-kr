---
title: 컴파일러 오류 C2279 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2279
dev_langs:
- C++
helpviewer_keywords:
- C2279
ms.assetid: 1b5c88ef-2336-49b8-9ddb-d61f97c73e14
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d1b194476e6400618045324a14c9e4781f9ec8f0
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46067950"
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