---
title: 컴파일러 경고 (수준 3) C4390 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4390
dev_langs:
- C++
helpviewer_keywords:
- C4390
ms.assetid: c95c2f1b-9bce-4b1f-a80c-565d4cde0b1e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 83131119e360bcf8193c2d6c8ca5a3cd09341516
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46054196"
---
# <a name="compiler-warning-level-3-c4390"></a>컴파일러 경고(수준 3) C4390

';': 제어 된 빈 문이 반환 합니다. 의도 입니까?

명령이 없는 제어 문의 한 후 세미콜론을 찾을 수 있습니다.

매크로 때문 C4390를 표시 하는 경우 사용 해야 합니다 [경고](../../preprocessor/warning.md) pragma 매크로 포함 하는 모듈에서 C4390를 사용 하지 않도록 설정 합니다.

다음 샘플에서는 C4390 오류가 생성 됩니다.

```
// C4390.cpp
// compile with: /W3
int main() {
   int i = 0;
   if (i);   // C4390
      i++;
}
```