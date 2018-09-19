---
title: 컴파일러 오류 C3285 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3285
dev_langs:
- C++
helpviewer_keywords:
- C3285
ms.assetid: 04e8f210-d67e-4810-b153-e1efe2986c8f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 685d83f224cc0b6c259a2fdf6946f28d909a1e6b
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46049568"
---
# <a name="compiler-error-c3285"></a>컴파일러 오류 C3285

for each 문은 'type' 형식의 변수에 사용할 수 없습니다.

`for each` 문은 배열 또는 개체 컬렉션의 각 요소에 대해 포함된 문 그룹을 반복합니다.

자세한 내용은 [for each, in](../../dotnet/for-each-in.md) 를 참조하세요.

## <a name="example"></a>예제

다음 샘플에서는 C3285를 생성합니다.

```
// C3285.cpp
// compile with: /clr
int main() {
   for each (int i in 0) {}   // C3285

   array<int> ^p = { 1, 2, 3 };
   for each (int j in p) {}   // OK
}
```