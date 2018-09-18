---
title: 컴파일러 경고 (수준 1) C4353 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4353
dev_langs:
- C++
helpviewer_keywords:
- C4353
ms.assetid: 6e79f186-ed82-4c95-9923-0ad5bb9c4db1
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 3926de61cdc41464c14c8610fee3033d10076506
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46066845"
---
# <a name="compiler-warning-level-1-c4353"></a>컴파일러 경고(수준 1) C4353

비표준 확장이 사용 됨: 함수 식으로 상수 0입니다. 내장 '__noop' 함수를 대신 사용

함수 식으로 상수 0 (0)를 사용할 수 없습니다. 자세한 내용은 [__noop](../../intrinsics/noop.md)합니다.

다음 샘플에서는 C4353 오류가 생성 됩니다.

```
// C4353.cpp
// compile with: /W1
void MyPrintf(void){};
#define X 0
#if X
   #define DBPRINT MyPrint
#else
   #define DBPRINT 0   // C4353 expected
#endif
int main(){
DBPRINT();
}
```