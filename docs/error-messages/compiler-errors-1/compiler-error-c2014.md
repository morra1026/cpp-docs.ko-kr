---
title: 컴파일러 오류 C2014
ms.date: 11/04/2016
f1_keywords:
- C2014
helpviewer_keywords:
- C2014
ms.assetid: 231d8e9c-48c0-4027-99a3-245d186275ec
ms.openlocfilehash: 58cf9867a9e36b304ab9da79084bc01dff453892
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50462662"
---
# <a name="compiler-error-c2014"></a>컴파일러 오류 C2014

전처리기 명령은 공백 아닌 문자로 시작 해야 합니다.

`#` 전처리기 지시문의 기호는 공백 없는 줄에 첫 번째 문자 여야 합니다.

다음 샘플에서는 C2014 오류가 생성 됩니다.

```
// C2014.cpp
int k; #include <stdio.h>   // C2014
```

해결 방법:

```
// C2014b.cpp
// compile with: /c
int k;
#include <stdio.h>
```