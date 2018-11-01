---
title: A.2   조건부 컴파일 지정
ms.date: 11/04/2016
ms.assetid: de4a21b9-f987-4738-9f13-c4795f6f2dff
ms.openlocfilehash: 92ae22ffac1b1a1c3fc45a9a7a883203ff6d251e
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50491223"
---
# <a name="a2---specifying-conditional-compilation"></a>A.2   조건부 컴파일 지정

다음 예제에서는 OpenMP 매크로 사용 하 여 조건부 컴파일 사용법을 보여 줍니다 `_OPENMP` ([섹션 2.2](../../parallel/openmp/2-2-conditional-compilation.md) 8 페이지). OpenMP 컴파일으로는 `_OPENMP` 매크로가 정의 됩니다.

```
# ifdef _OPENMP
    printf_s("Compiled by an OpenMP-compliant implementation.\n");
# endif
```

정의 된 전처리기 연산자에는 둘 이상의 매크로 단일 지시문에서 테스트할 수 있습니다.

```
# if defined(_OPENMP) && defined(VERBOSE)
    printf_s("Compiled by an OpenMP-compliant implementation.\n");
# endif
```