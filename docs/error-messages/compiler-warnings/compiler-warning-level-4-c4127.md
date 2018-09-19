---
title: 컴파일러 경고 (수준 4) C4127 | Microsoft Docs
ms.custom: ''
ms.date: 09/13/2018
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4127
dev_langs:
- C++
helpviewer_keywords:
- C4127
ms.assetid: f59ded9e-5227-45bd-ac43-2aa861581363
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 561173e2b451a0b736d97042667a2fb14b3a7eb7
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46094899"
---
# <a name="compiler-warning-level-4-c4127"></a>컴파일러 경고(수준 4) C4127

> 조건식이 상수입니다.

## <a name="remarks"></a>설명

`if` 문 또는 `while` 루프의 제어 식이 상수로 계산됩니다. Visual Studio 2015 업데이트 3, 1과 같은 특수 상수부터 해당 일반적인 관용구 사용으로 인해 또는 `true` 식에서 연산의 결과가 아닌 경고를 트리거하지 않습니다.

하는 경우의 제어 식이 `while` 루프는 루프가 중간에 종료 때문에 상수를 바꾸는 것이 좋습니다는 `while` 루프를 `for` 루프입니다. 초기화, 종료 테스트를 생략 하 고 루프의 증가 `for` 인해 마찬가지로 무한 루프가 있는 루프 `while(1)`, 본문에서 루프를 종료할 수 있습니다는 `for` 문입니다.

## <a name="example"></a>예제

다음 샘플에서는 두 가지 방법으로 C4127 생성 되 고 사용 하는 방법을 보여 줍니다는 for 루프 경고를 방지 하려면:

```cpp
// C4127.cpp
// compile with: /W4
#include <stdio.h>
int main() {
   if (true) {}           // OK in VS2015 update 3 and later
   if (1 == 1) {}         // C4127
   while (42) { break; }  // C4127

   // OK
   for ( ; ; ) {
      printf("test\n");
      break;
   }
}
```