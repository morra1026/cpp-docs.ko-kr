---
title: 컴파일러 오류 C2790 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2790
dev_langs:
- C++
helpviewer_keywords:
- C2790
ms.assetid: 38d4fce1-ba00-413d-8bc1-e8aa43d7bc1f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: dc2c6b238fab7e42c0754e613b62756a86a5bb31
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46069575"
---
# <a name="compiler-error-c2790"></a>컴파일러 오류 C2790

'super':이 키워드는 클래스 멤버 함수의 본문 내 에서만 사용할 수 있습니다

키워드를 사용 하는 사용자가 하려고 할 경우이 오류 메시지가 나타납니다 [super](../../cpp/super.md) 멤버 함수의 컨텍스트 외부에서.

다음 샘플에서는 C2790를 생성합니다.

```
// C2790.cpp
void f() {
   __super::g();   // C2790
}
```