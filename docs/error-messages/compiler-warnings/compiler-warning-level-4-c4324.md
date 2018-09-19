---
title: 컴파일러 경고 (수준 4) C4324 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4324
dev_langs:
- C++
helpviewer_keywords:
- C4324
ms.assetid: 420fa929-d9c0-40b4-8808-2d8ad3ca8090
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 2499aa7c674e3bd1bece14c39b09f9863d6bb783
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46064791"
---
# <a name="compiler-warning-level-4-c4324"></a>컴파일러 경고(수준 4) C4324

'struct_name': __declspec(align()) 때문에 구조체가 채워졌습니다

안쪽 여백을 지정 했기 때문에 구조체의 끝에 추가 된를 [__declspec (align)](../../cpp/align-cpp.md) 값입니다.

예를 들어, 다음 코드에서는 C4324를 생성합니다.

```
// C4324.cpp
// compile with: /W4
struct __declspec(align(32)) A
{
   char a;
};   // C4324

int main()
{
}
```