---
title: 컴파일러 오류 C3874
ms.date: 11/04/2016
f1_keywords:
- C3874
helpviewer_keywords:
- C3874
ms.assetid: fd55fc05-69a7-4237-b3b7-dca1d5400b4f
ms.openlocfilehash: 73476d50b6cfe098ee9d8084837c2090e198a6cd
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50445047"
---
# <a name="compiler-error-c3874"></a>컴파일러 오류 C3874

'function'의 반환 형식 'type' 대신 ' int' 해야 합니다.

함수에는 컴파일러에서 예상 된 반환 형식이 없습니다.

다음 샘플에서는 C3874 오류가 생성 됩니다.

```
// C3874b.cpp
double main()
{   // C3874
}
```