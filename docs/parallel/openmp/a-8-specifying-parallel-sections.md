---
title: A.8 Parallel Sections 지정 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: cf399304-121e-4c07-9829-47e0dbc2ef10
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 9d969f1a0e9d9b282104ee00a3b2d06610533ad4
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46440422"
---
# <a name="a8---specifying-parallel-sections"></a>A.8   Parallel Sections 지정

다음 예에서 (에 대 한 [2.4.2 섹션](../../parallel/openmp/2-4-2-sections-construct.md) 14 페이지) 함수 *x 축*합니다 *yaxis*, 및 *zaxis* 동시에 실행할 수 있습니다. 첫 번째 `section` 지시문은 선택 사항입니다.  모든 `section` 지시문의 어휘 범위에 표시 되어야 합니다 `parallel sections` 생성 합니다.

```
#pragma omp parallel sections
{
    #pragma omp section
        xaxis();
    #pragma omp section
        yaxis();
    #pragma omp section
        zaxis();
}
```