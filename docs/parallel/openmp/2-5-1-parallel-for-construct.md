---
title: 2.5.1 parallel for 구문 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: a233e7ed-2462-4f7a-9a5d-556ab9f363d8
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: cfff3b0c17dd098b5d802af61a7ca1f81cb02845
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46373963"
---
# <a name="251-parallel-for-construct"></a>2.5.1 parallel for 구문

합니다 **에 대 한 병렬** 지시문에 대 한 바로 가기입니다를 **병렬** 하나만 포함 하는 영역 **에 대 한** 지시문입니다. 구문의 합니다 **에 대 한 병렬** 지시문은 다음과 같습니다.

```
#pragma omp parallel for [clause[[,] clause] ...] new-linefor-loop
```

이 지시문의 절을 사용 합니다 **병렬** 지시문 및 **에 대 한** 지시문을 제외 하 고는 `nowait` 동일한 의미 및 제한 사항으로 절. 의미 체계는 동일 명시적으로 지정 하는 **병렬** 지시문 바로 뒤에 **에 대 한** 지시문입니다.

## <a name="cross-references"></a>교차 참조:

- **병렬** 지시문을 참조 하십시오 [섹션 2.3](../../parallel/openmp/2-3-parallel-construct.md) 8 페이지입니다.

- **에 대 한** 지시문을 참조 하십시오 [2.4.1 섹션](../../parallel/openmp/2-4-1-for-construct.md) 11 페이지입니다.

- 데이터 특성 절을 참조 하세요 [2.7.2 데이터 공유 특성 절](../../parallel/openmp/2-7-2-data-sharing-attribute-clauses.md) 25 페이지입니다.