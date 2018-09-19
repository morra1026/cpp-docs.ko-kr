---
title: 컴파일러 오류 C2801 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2801
dev_langs:
- C++
helpviewer_keywords:
- C2801
ms.assetid: 35dfc7ea-9e37-4e30-baa1-944dc61302f5
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d57ee5bf5f5152ef55852c9f9b829bc4a1d17d41
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46040637"
---
# <a name="compiler-error-c2801"></a>컴파일러 오류 C2801

'operator o p 비정적 멤버 여야 합니다.

비정적 멤버로 다음과 같은 연산자를 오버 로드할 수 있습니다.

- 할당 `=`

- 클래스 멤버 액세스 `->`

- 첨자 `[]`

- 함수 호출 `()`

가능한 C2801 원인:

- 오버 로드 된 연산자는 클래스, 구조체 또는 공용 구조체 멤버 아닙니다.

- 오버 로드 된 연산자를 선언 했습니다 `static`합니다.

- 다음 샘플에서는 C2801를 생성합니다.

```
// C2801.cpp
// compile with: /c
operator[]();   // C2801 not a member
class A {
   static operator->();   // C2801 static
   operator()();   // OK
};
```