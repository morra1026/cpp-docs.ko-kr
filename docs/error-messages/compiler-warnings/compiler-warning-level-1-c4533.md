---
title: 컴파일러 경고 (수준 1) C4533 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4533
dev_langs:
- C++
helpviewer_keywords:
- C4533
ms.assetid: 359fecda-d540-46e5-b214-dbabe9ef50d2
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 1a99211afe310730e9041f2f04dc8ce67a762ed0
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46084863"
---
# <a name="compiler-warning-level-1-c4533"></a>컴파일러 경고(수준 1) C4533

'variable' 초기화 '명령을' 의해 생략 되었습니다.

명령 프로그램에서 변경, 제어 흐름, 변수를 초기화 하는 명령이 실행 되지 않았습니다. 다음 샘플에서는 C4533 오류가 생성 됩니다.

```
// C4533.cpp
// compile with: /W1
#include <stdio.h>

struct A
{
   int m_data;
};

int main()
{
   if (1)
   {
      goto Label;
   }

   A a = { 100 };

   Label:   // C4533
      printf("\n%d", a.m_data);   // prints an uninitialized value
}
```