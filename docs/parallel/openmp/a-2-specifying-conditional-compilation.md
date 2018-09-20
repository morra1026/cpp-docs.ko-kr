---
title: A.2 조건부 컴파일 지정 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: de4a21b9-f987-4738-9f13-c4795f6f2dff
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 2d8b0f3df67313dbf03d40077a551fe64930199d
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46393700"
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