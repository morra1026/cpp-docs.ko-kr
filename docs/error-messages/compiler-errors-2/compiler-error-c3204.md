---
title: 컴파일러 오류 C3204
ms.date: 11/04/2016
f1_keywords:
- C3204
helpviewer_keywords:
- C3204
ms.assetid: 06e578da-0262-48c8-b2ae-be1cd6d28884
ms.openlocfilehash: 4c34ad35916f01323a72102c7099d4afd0ab17be
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50539297"
---
# <a name="compiler-error-c3204"></a>컴파일러 오류 C3204

'_alloca'는 catch 블록 내부에서 호출할 수 없습니다.

이 오류는 catch 블록 내에서 [_alloca](../../c-runtime-library/reference/alloca.md) 호출을 사용하는 경우에 발생합니다.

## <a name="example"></a>예제

다음 샘플에서는 C3204를 생성합니다.

```
// C3204.cpp
// compile with: /EHsc
#include <malloc.h>

void ShowError(void)
{
   try
   {
   }
   catch(...)
   {
      _alloca(1);   // C3204
   }
}
```