---
title: 컴파일러 오류 C2650
ms.date: 11/04/2016
f1_keywords:
- C2650
helpviewer_keywords:
- C2650
ms.assetid: 49a8ac6e-aa6d-4616-917c-a3cfcdbad5a4
ms.openlocfilehash: c7cbc12bff4e00613032a9d28b5be7533dce9612
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50608002"
---
# <a name="compiler-error-c2650"></a>컴파일러 오류 C2650

'operator': 가상 함수 일 수 없습니다.

A `new` 나 `delete` 연산자를 선언 했습니다 `virtual`합니다. 이러한 연산자는 `static` 멤버 함수 및이 하 여야 `virtual`합니다.

## <a name="example"></a>예제

다음 샘플에서는 C2650를 생성합니다.

```
// C2650.cpp
// compile with: /c
class A {
   virtual void* operator new( unsigned int );   // C2650
   // try the following line instead
   // void* operator new( unsigned int );
};
```