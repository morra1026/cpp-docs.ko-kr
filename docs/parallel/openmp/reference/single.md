---
title: 단일 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
f1_keywords:
- Single
dev_langs:
- C++
helpviewer_keywords:
- single OpenMP directive
ms.assetid: 85cf94fb-cb9c-4d82-8609-adffa9f552e1
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 2fadd4f9789dc834c1bae0477c828892fed94b5c
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46413369"
---
# <a name="single"></a>단일

코드의 섹션 마스터 스레드 반드시 단일 스레드에서 실행할지를 지정할 수 있습니다.

## <a name="syntax"></a>구문

```
#pragma omp single [clauses] 
{
   code_block
}
```

#### <a name="parameters"></a>매개 변수

*절*<br/>
(선택 사항) 0 개 이상의 절입니다. 지 원하는 절의 목록 설명 섹션을 참조 하세요 **단일**합니다.

## <a name="remarks"></a>설명

합니다 **단일** 지시문 다음 OpenMP 절을 지원 합니다.

- [copyprivate](../../../parallel/openmp/reference/copyprivate.md)

- [firstprivate](../../../parallel/openmp/reference/firstprivate.md)

- [nowait](../../../parallel/openmp/reference/nowait.md)

- [private](../../../parallel/openmp/reference/private-openmp.md)

합니다 [마스터](../../../parallel/openmp/reference/master.md) 지시어를 사용 하면 코드의 섹션은 마스터 스레드에서만 실행 되도록 지정 합니다.

자세한 내용은 [2.4.3 single 생성](../../../parallel/openmp/2-4-3-single-construct.md)합니다.

## <a name="example"></a>예제

```cpp
// omp_single.cpp
// compile with: /openmp
#include <stdio.h>
#include <omp.h>

int main() {
   #pragma omp parallel num_threads(2)
   {
      #pragma omp single
      // Only a single thread can read the input.
      printf_s("read input\n");

      // Multiple threads in the team compute the results.
      printf_s("compute results\n");

      #pragma omp single
      // Only a single thread can write the output.
      printf_s("write output\n");
    }
}
```

```Output
read input
compute results
compute results
write output
```

## <a name="see-also"></a>참고 항목

[지시문](../../../parallel/openmp/reference/openmp-directives.md)