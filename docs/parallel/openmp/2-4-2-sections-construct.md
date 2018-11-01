---
title: 2.4.2 sections 구문
ms.date: 11/04/2016
ms.assetid: e9e6e3ea-7fc9-4925-8f68-92b8a5bb1e76
ms.openlocfilehash: 2d9fca08eecd382c9d3df60159c13ac188a1ab85
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50486816"
---
# <a name="242-sections-construct"></a>2.4.2 sections 구문

합니다 **섹션에서는** 지시문 팀에서 스레드로 분배 하는 구문 집합을 지정 하는 noniterative 작업 공유 구문으로 식별 합니다. 각 섹션은 팀의 스레드에 의해 한 번 실행 됩니다. 구문의 합니다 **섹션에서는** 지시문은 다음과 같습니다.

```
#pragma omp sections [clause[[,] clause] ...] new-line
   {
   [#pragma omp section new-line]
      structured-block
   [#pragma omp section new-linestructured-block ]
...
}
```

절은 다음 중 하나입니다.

**private(** *variable-list* **)**

**firstprivate(** *variable-list* **)**

**lastprivate(** *variable-list* **)**

**reduction(** *operator* **:**  *variable-list* **)**

**nowait**

각 섹션 앞에 **섹션** 지시문을 있지만 합니다 **섹션** 지시문은 첫 번째 섹션에 대 한 선택 사항. 합니다 **섹션** 지시문의 어휘 범위 내에 나타나야 합니다 합니다 **섹션** 지시문입니다. 끝에는 암시적 장벽이를 **섹션** 하지 않는 경우 생성할를 **nowait** 지정 됩니다.

에 대 한 제한 된 **섹션** 지시문은 다음과 같습니다.

- A **섹션** 지시문의 어휘 범위 외부에 나타나지 않아야 합니다 **섹션** 지시문입니다.

- 단일 **nowait** 절에 나타날 수 있습니다는 **섹션** 지시문입니다.

## <a name="cross-references"></a>교차 참조:

- **개인**, **firstprivate**, **lastprivate**, 및 **감소** 절을 참조 하십시오 [섹션 2.7.2](../../parallel/openmp/2-7-2-data-sharing-attribute-clauses.md) 25 페이지입니다.