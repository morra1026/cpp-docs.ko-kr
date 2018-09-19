---
title: 컴파일러 오류 C2041 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2041
dev_langs:
- C++
helpviewer_keywords:
- C2041
ms.assetid: c9a33bb1-f9cf-47d6-bd21-7d867a8c37d5
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: bee199ea3ddca7ae329fc17ed6c3c013dc460eb7
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46082172"
---
# <a name="compiler-error-c2041"></a>컴파일러 오류 C2041

'character' 기본 'number'에 대 한 숫자가 잘못 되었습니다

지정된 된 문자 (예: 8 진수 또는 16 진수) 기준에 유효한 숫자가 아닙니다.

다음 샘플에서는 C2041 오류가 생성 됩니다.

```
// C2041.cpp
int i = 081;   // C2041  8 is not a base 8 digit
```

해결 방법:

```
// C2041b.cpp
// compile with: /c
int j = 071;
```