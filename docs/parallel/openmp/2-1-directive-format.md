---
title: 2.1 지시문 형식 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 918b6445-d35e-4176-9565-b045be941b4d
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 1b2f2d2f5742dbc4faa1d8386e935c9d4ccc8049
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46424653"
---
# <a name="21-directive-format"></a>2.1 지시문 형식

OpenMP 지시문의 구문은 문법을 공식적으로 지정 된 [부록 C](../../parallel/openmp/c-openmp-c-and-cpp-grammar.md)에서 같이 비공식적으로:

```
#pragma omp directive-name  [clause[ [,] clause]...] new-line
```

로 시작 하는 각 지시문 **#pragma omp**를 같은 이름의 다른 (openmp-OpenMP 또는 공급 업체 확장) pragma 지시문을 사용 하 여 충돌을 방지 합니다. 지시문의 나머지 부분에는 컴파일러 지시문에 대 한 C 및 c + + 표준 규칙을 따릅니다. 특히, 공백을 사용할 수 앞과 뒤의 **#**, 및 경우에 따라 지시문에서 단어를 구분 하려면 공백을 사용 해야 합니다. 다음 토큰을 전처리 합니다 **#pragma omp** 매크로 대체 될 수 있습니다.

지시문 대/소문자를 구분 하지 않습니다. 지시문의 절이 표시 되는 순서는 중요 하지 않습니다. 각 절에 대 한 설명을에 나열 된 제한이 필요에 따라 지시문에 절을 반복 될 수 있습니다. 하는 경우 *변수 목록* 절에만 변수를 지정 해야 표시 됩니다. 하나만 *지시문 이름* 지시문에 따라 지정할 수 있습니다.  예를 들어 다음 지시문은 사용할 수 없습니다.

```
/* ERROR - multiple directive names not allowed */
#pragma omp parallel barrier
```

최대 하나의 후속 문, 구조화 된 블록 이어야 하는 OpenMP 지시문에 적용 됩니다.