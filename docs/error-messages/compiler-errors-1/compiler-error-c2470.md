---
title: 컴파일러 오류 C2470 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2470
dev_langs:
- C++
helpviewer_keywords:
- C2470
ms.assetid: e17d2cb8-b84c-447c-976a-625f0c96f3fe
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 8f494f550393bf1fb1a1a17b522b73945a7581e6
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46089153"
---
# <a name="compiler-error-c2470"></a>컴파일러 오류 C2470

'function': 함수 정의 보이지만 매개 변수 목록이 없습니다. 명백한 본문을 건너뜁니다.

함수 정의 인수 목록이 없습니다.

다음 샘플에서는 C2470 오류가 생성 됩니다.

```
// C2470.cpp
int MyFunc {};  // C2470
void MyFunc2() {};  //OK

int main(){
   MyFunc();
   MyFunc2();
}
```