---
title: 컴파일러 경고 (수준 1) C4329 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4329
dev_langs:
- C++
helpviewer_keywords:
- C4329
ms.assetid: 4316f51a-2c56-4b3f-831e-65d24b83b65c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 6f4d250bbd21e55a64009522e5f277493730f7d1
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46084902"
---
# <a name="compiler-warning-level-1-c4329"></a>컴파일러 경고(수준 1) C4329

__declspec(align())는 enum에서 무시 됩니다.

사용 합니다 [맞춤](../../cpp/align-cpp.md) 키워드는 [__declspec](../../cpp/declspec.md) 한정자에서 허용 되지 않습니다는 `enum`합니다. 다음 샘플에서는 C4329 오류가 생성 됩니다.

```
// C4329.cpp
// compile with: /W1 /LD
enum __declspec(align(256)) TestEnum {   // C4329
   TESTVAL1,
   TESTVAL2,
   TESTVAL3
};
__declspec(align(256)) enum TestEnum1;
```