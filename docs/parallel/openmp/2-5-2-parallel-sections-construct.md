---
title: 2.5.2 parallel sections 구문 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 94220e27-14f8-465c-bd8d-eb960b4b5dee
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 073d0561fe4bfbb96ed88681a077da6fc985c963
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46402332"
---
# <a name="252-parallel-sections-construct"></a>2.5.2 parallel sections 구문

**섹션에서는 병렬** 지시어를 지정 하기 위한 바로 가기 양식을 제공를 **병렬** 지역 하나만 포함 된 **섹션** 지시문입니다. 의미 체계는 동일 명시적으로 지정 하는 **병렬** 지시문 바로 뒤에 **섹션** 지시문입니다. 구문의 합니다 **섹션에서는 병렬** 지시문은 다음과 같습니다.

```
#pragma omp parallel sections  [clause[[,] clause] ...] new-line
   {
   [#pragma omp section new-line]
      structured-block
   [#pragma omp section new-linestructured-block  ]
   ...
}
```

*절* 수락한 절 중 하나일 수 있습니다 합니다 **병렬** 및 **섹션** 지시문을 제외 하 고는 **nowait** 절.

## <a name="cross-references"></a>교차 참조:

- **병렬** 지시문을 참조 하십시오 [섹션 2.3](../../parallel/openmp/2-3-parallel-construct.md) 8 페이지입니다.

- **섹션** 지시문을 참조 하십시오 [2.4.2 섹션](../../parallel/openmp/2-4-2-sections-construct.md) 14 페이지입니다.