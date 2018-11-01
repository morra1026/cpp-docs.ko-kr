---
title: 컴파일러 오류 C2815
ms.date: 11/04/2016
f1_keywords:
- C2815
helpviewer_keywords:
- C2815
ms.assetid: d0256fd6-0721-4c99-b03c-52d96e77a613
ms.openlocfilehash: ab6708e7ae0a56bd71adebad4fb42d6ea9abe116
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50432658"
---
# <a name="compiler-error-c2815"></a>컴파일러 오류 C2815

operator delete': 첫 번째 정식 매개 변수 이어야 ' void *', 'param' 사용한 하지만

모든 사용자 정의 [delete 연산자](../../standard-library/new-operators.md#op_delete) 함수 형식의 첫 번째 정식 매개 변수를 취해야 `void *`합니다.

다음 샘플에서는 C2815 오류가 생성 됩니다.

```
// C2815.cpp
// compile with: /c
class CMyClass {
public:
   void mf1(int *a);
   void operator delete(CMyClass *);   // C2815
   void operator delete(void *);
};
```