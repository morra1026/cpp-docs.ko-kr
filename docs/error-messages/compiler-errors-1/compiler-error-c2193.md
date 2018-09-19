---
title: 컴파일러 오류 C2193 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2193
dev_langs:
- C++
helpviewer_keywords:
- C2193
ms.assetid: 9813e853-d581-4f51-bb75-4e242298a844
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ecfadd6476b8ed65891b5cb8fcbb3e0d54b203ce
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46071460"
---
# <a name="compiler-error-c2193"></a>컴파일러 오류 C2193

'identifier': 세그먼트에 이미

함수를 사용 하 여 두 개의 서로 다른 세그먼트에 배치 되었습니다 `alloc_text` 고 `code_seg` pragma입니다.

다음 샘플에서는 C2193 오류가 생성 됩니다.

```
// C2193.cpp
// compile with: /c
extern "C" void MYFUNCTION();
#pragma alloc_text(MYCODE, MYFUNCTION)
#pragma code_seg("MYCODE2")
extern "C" void MYFUNCTION() {}   // C2193
extern "C" void MYFUNCTION2() {}
```