---
title: sections (OpenMP) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
f1_keywords:
- section
- SECTIONS
dev_langs:
- C++
helpviewer_keywords:
- sections OpenMP directive
ms.assetid: 4cd1d776-e198-470e-930a-01fb0ab0a0bd
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 32dab6784e4265432f596b585e098f6a77687117
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46421546"
---
# <a name="sections-openmp"></a>sections (OpenMP)

모든 스레드 간에 나눌 코드 섹션을 식별 합니다.

## <a name="syntax"></a>구문

```
#pragma omp [parallel] sections [clauses]
{
   #pragma omp section
   {
      code_block
   } 
}
```

## <a name="arguments"></a>인수

*절*<br/>
(선택 사항) 0 개 이상의 절입니다. 지 원하는 절의 목록 설명 섹션을 참조 하세요 **섹션에서는**합니다.

## <a name="remarks"></a>설명

합니다 **섹션이** 지시문에는 0 개 이상 포함 될 수 있습니다 **섹션** 지시문입니다.

합니다 **섹션에서는** 지시문 다음 OpenMP 절을 지원 합니다.

- [firstprivate](../../../parallel/openmp/reference/firstprivate.md)

- [lastprivate](../../../parallel/openmp/reference/lastprivate.md)

- [nowait](../../../parallel/openmp/reference/nowait.md)

- [private](../../../parallel/openmp/reference/private-openmp.md)

- [reduction](../../../parallel/openmp/reference/reduction.md)

하는 경우 **병렬** 도 지정 되어 `clause` 절에서 사용할 수는 **병렬** 또는 **섹션** 지시문을 제외한 `nowait`합니다.

자세한 내용은 [2.4.2 sections 구문](../../../parallel/openmp/2-4-2-sections-construct.md)합니다.

## <a name="example"></a>예제

```
// omp_sections.cpp
// compile with: /openmp
#include <stdio.h>
#include <omp.h>

int main() {
    #pragma omp parallel sections num_threads(4)
    {
        printf_s("Hello from thread %d\n", omp_get_thread_num());
        #pragma omp section
        printf_s("Hello from thread %d\n", omp_get_thread_num());
    }
}
```

```Output
Hello from thread 0
Hello from thread 0
```

## <a name="see-also"></a>참고 항목

[지시문](../../../parallel/openmp/reference/openmp-directives.md)