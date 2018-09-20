---
title: 4.3 OMP_DYNAMIC | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: a15edefb-1f85-4f06-a427-beb3cfc4434f
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: c15fa9d8c9d86b736bfc577a3b17e9809ec9baaf
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46439200"
---
# <a name="43-ompdynamic"></a>4.3 OMP_DYNAMIC

합니다 **OMP_DYNAMIC** 환경 변수 사용 하거나 동적으로 조정 하는 명시적으로 사용 하도록 설정 하거나 를호출하여사용하지않도록설정하지않는한병렬영역실행에사용가능한스레드수를동적으로조정을사용하지않도록설정**omp_set_dynamic** 라이브러리 루틴입니다. 해당 값 이어야 합니다 **TRUE** 하거나 **FALSE**합니다.

경우 설정 **TRUE**, 시스템 리소스를 최대한 활용 하려면 런타임 환경에서 병렬 영역을 실행 하는 데 사용 되는 스레드 수가 조정 될 수 있습니다.  경우로 **FALSE**를 동적으로 조정 하는 사용 하지 않도록 설정 합니다. 기본 조건을 구현 시 정의 됩니다.

예제:

```
setenv OMP_DYNAMIC TRUE
```

## <a name="cross-references"></a>교차 참조:

- 병렬 영역에 대 한 자세한 내용은 참조 하세요. [섹션 2.3](../../parallel/openmp/2-3-parallel-construct.md) 8 페이지입니다.

- **omp_set_dynamic** 함수를 참조 하세요 [3.1.7 섹션](../../parallel/openmp/3-1-7-omp-set-dynamic-function.md) 39 페이지입니다.