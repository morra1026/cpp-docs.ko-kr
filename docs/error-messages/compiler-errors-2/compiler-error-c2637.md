---
title: 컴파일러 오류 C2637 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2637
dev_langs:
- C++
helpviewer_keywords:
- C2637
ms.assetid: 58d94447-eb96-4d8f-a690-dd78d322462e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 6242183e1510565ece7d75085657764b1ddc4081
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46101479"
---
# <a name="compiler-error-c2637"></a>컴파일러 오류 C2637

'identifier': 데이터 멤버에 대 한 포인터를 수정할 수 없습니다.

데이터 멤버에 대 한 포인터는 호출 규칙을 사용할 수 없습니다. 를 해결 하려면 호출 규칙을 제거 하거나 멤버 함수에 대 한 포인터를 선언 합니다.

다음 샘플에서는 C2637 오류가 생성 됩니다.

```
// C2637.cpp
// compile with: /c
struct S {};
int __stdcall S::*pms1;   // C2637

// OK
int S::*pms2;
int (__stdcall S::*pms3)(...);
```