---
title: 컴파일러 오류 C2195 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2195
dev_langs:
- C++
helpviewer_keywords:
- C2195
ms.assetid: 9f9f035c-9c51-4173-a8ea-c6f907fc5c63
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 2ec81b9c720d1dfc5a629faaa74fb321cdf93b4b
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46020606"
---
# <a name="compiler-error-c2195"></a>컴파일러 오류 C2195

'identifier': 데이터 세그먼트

합니다 `code_seg` pragma를 사용 하는 세그먼트 이름을 사용 합니다 `data_seg` pragma입니다.

다음 샘플에서는 C2195 오류가 생성 됩니다.

```
// C2195.cpp
#pragma data_seg("MYDATA")
#pragma code_seg("MYDATA")   // C2195
#pragma code_seg("MYDATA2")   // OK
```