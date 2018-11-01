---
title: 컴파일러 오류 C3003
ms.date: 11/04/2016
f1_keywords:
- C3003
helpviewer_keywords:
- C3003
ms.assetid: 22e74f99-bb7f-4518-ab0d-934d5d49bcc7
ms.openlocfilehash: 6d15d8bde8855b8dcc4857492acdeb950731b503
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50537555"
---
# <a name="compiler-error-c3003"></a>컴파일러 오류 C3003

'directive': 지시문 절 다음에는 OpenMP 지시문 이름이 올 수 없습니다.

OpenMP 지시문 이름이 OpenMP 지시문 절 다음에 올 수 없습니다.

다음 샘플에서는 C3003을 생성합니다.

```
// C3003.c
// compile with: /openmp
int main()
{
   int x, y, z;
   #pragma omp parallel shared(x, y, z) for   // C3003
}
```