---
title: 컴파일러 오류 C2194 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2194
dev_langs:
- C++
helpviewer_keywords:
- C2194
ms.assetid: df6e631c-0062-4844-9088-4cc7a0ff879f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 6270835b75181abcc683ac8d625d6d9236ae2b95
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46035801"
---
# <a name="compiler-error-c2194"></a>컴파일러 오류 C2194

'identifier': 텍스트 세그먼트

합니다 `data_seg` pragma를 사용 하는 세그먼트 이름이 사용 `code_seg`합니다.

다음 샘플에서는 C2194 오류가 생성 됩니다.

```
// C2194.cpp
// compile with: /c
#pragma code_seg("MYCODE")
#pragma data_seg("MYCODE")   // C2194
#pragma data_seg("MYCODE2")   // OK
```