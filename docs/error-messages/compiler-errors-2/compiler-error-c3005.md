---
title: 컴파일러 오류 C3005
ms.date: 11/04/2016
f1_keywords:
- C3005
helpviewer_keywords:
- C3005
ms.assetid: 30bad565-e79f-4c3f-82cb-a74bd0baab8f
ms.openlocfilehash: 1303fd667c92af6fd8d0476da9468b4c7d090e6b
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50444306"
---
# <a name="compiler-error-c3005"></a>컴파일러 오류 C3005

'error_text': OpenMP 'directive' 지시문에 예기치 못한 토큰이 있습니다.

OpenMP 지시문 형식이 잘못되었습니다.

다음 샘플에서는 C3005를 생성합니다.

```
// C3005.c
// compile with: /openmp
int main()
{
   #pragma omp parallel + for   // C3005
}
```

C3005는 pragma와 같은 줄에 여는 중괄호를 배치하면 발생할 수 있습니다.

```
// C3005b.c
// compile with: /openmp
int main() {
   #pragma omp parallel {   // C3005 put open brace on next line
   lbl2:;
   }
   goto lbl2;
}
```