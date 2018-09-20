---
title: 병렬 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
f1_keywords:
- parallel
dev_langs:
- C++
helpviewer_keywords:
- parallel OpenMP directive
ms.assetid: b8e90073-e85b-4d39-8ed8-0364441794fb
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 38b5bd4d277987be78cbd3714302c8b7f704b90f
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46405218"
---
# <a name="parallel"></a>parallel

병렬로 여러 스레드에서 실행 될 코드는 병렬 영역을 정의 합니다.

## <a name="syntax"></a>구문

```
#pragma omp parallel [clauses]
{
   code_block
}
```

## <a name="arguments"></a>인수

*절*<br/>
(선택 사항) 0 개 이상의 절입니다.  지 원하는 절의 목록 설명 섹션을 참조 하세요 **병렬**합니다.

## <a name="remarks"></a>설명

합니다 **병렬** 지시문 다음 OpenMP 절을 지원 합니다.

- [copyin](../../../parallel/openmp/reference/copyin.md)

- [default](../../../parallel/openmp/reference/default-openmp.md)

- [firstprivate](../../../parallel/openmp/reference/firstprivate.md)

- [if](../../../parallel/openmp/reference/if-openmp.md)

- [num_threads](../../../parallel/openmp/reference/num-threads.md)

- [private](../../../parallel/openmp/reference/private-openmp.md)

- [reduction](../../../parallel/openmp/reference/reduction.md)

- [shared](../../../parallel/openmp/reference/shared-openmp.md)

**병렬** 사용 하 여 사용할 수도 있습니다는 [섹션](../../../parallel/openmp/reference/sections-openmp.md) 하 고 [에 대 한](../../../parallel/openmp/reference/for-openmp.md) 지시문입니다.

자세한 내용은 [2.3 parallel 구문](../../../parallel/openmp/2-3-parallel-construct.md)합니다.

## <a name="example"></a>예제

다음 샘플에는 스레드 수를 설정 하 고 병렬 영역을 정의 하는 방법을 보여 줍니다. 기본적으로 스레드 수가 컴퓨터의 논리 프로세서의 수와 같습니다. 예를 들어, 하이퍼 스레딩을 사용에 실제 프로세서가 있는 컴퓨터에 있는 경우 됩니다 것 두 개의 논리 프로세서 및 따라서 두 개의 스레드입니다.

```
// omp_parallel.cpp
// compile with: /openmp
#include <stdio.h>
#include <omp.h>

int main() {
   #pragma omp parallel num_threads(4)
   {
      int i = omp_get_thread_num();
      printf_s("Hello from thread %d\n", i);
   }
}
```

```Output
Hello from thread 0
Hello from thread 1
Hello from thread 2
Hello from thread 3
```

## <a name="comment"></a>주석

출력의 순서는 서로 다른 컴퓨터에서 달라질 수 있는 참고 합니다.

## <a name="see-also"></a>참고 항목

[지시문](../../../parallel/openmp/reference/openmp-directives.md)