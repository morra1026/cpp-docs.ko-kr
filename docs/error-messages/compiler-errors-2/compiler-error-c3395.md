---
title: 컴파일러 오류 C3395 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3395
dev_langs:
- C++
helpviewer_keywords:
- C3395
ms.assetid: 26a9ebc9-ed97-47ce-b436-19aa2bcf6e50
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b604db63466df28d951e8c0027d85f55013f4d5a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46103427"
---
# <a name="compiler-error-c3395"></a>컴파일러 오류 C3395

'function': __declspec (dllexport)을 사용 하는 함수에 적용할 수 없습니다는 \__clrcall 호출 규칙

`__declspec(dllexport)` 및 [__clrcall](../../cpp/clrcall.md) 호환 되지 않습니다.  자세한 내용은 [dllexport, dllimport](../../cpp/dllexport-dllimport.md)합니다.

다음 샘플에서는 C3395 오류가 생성 됩니다.

```
// C3395.cpp
// compile with: /clr /c

__declspec(dllexport) void __clrcall Test(){}   // C3395
void __clrcall Test2(){}   // OK
__declspec(dllexport) void Test3(){}   // OK
```