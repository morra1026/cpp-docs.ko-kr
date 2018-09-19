---
title: 컴파일러 오류 C3626 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3626
dev_langs:
- C++
helpviewer_keywords:
- C3626
ms.assetid: 43926e2b-1ba9-4a43-9343-c58449cbb336
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ba6fb7c03c7c957999ca75e3946e4f78d290b78a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46094704"
---
# <a name="compiler-error-c3626"></a>컴파일러 오류 C3626

'keyword': '__event' 키워드는 COM 인터페이스, 멤버 함수 및 대리자에 대 한 포인터는 데이터 멤버에만 사용할 수 있습니다

키워드를 잘못 사용 했습니다.

다음 샘플에서는 C3626를 생성합니다.

```
// C3626.cpp
// compile with: /c
struct A {
   __event int i;   // C3626
// try the following line instead
// __event int i();
};
```