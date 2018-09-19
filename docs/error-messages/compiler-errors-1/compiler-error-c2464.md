---
title: 컴파일러 오류 C2464 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2464
dev_langs:
- C++
helpviewer_keywords:
- C2464
ms.assetid: ace953d6-b414-49ee-bfef-90578a8da00c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ff74085364d6638772ab2376aace93fea741056b
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46103147"
---
# <a name="compiler-error-c2464"></a>컴파일러 오류 C2464

'identifier': 참조를 할당 하는 데 'new' 사용할 수 없습니다

참조 식별자를 사용 하 여 할당 된 `new` 연산자입니다. 참조는 하므로 메모리 개체가 아니므로 `new` 에 대 한 포인터를 반환할 수 없습니다. 표준 변수 선언 구문을 사용 하 여 참조를 선언 합니다.

다음 샘플에서는 C2464를 생성합니다.

```
// C2464.cpp
int main() {
   new ( int& ir );   // C2464
}
```