---
title: 2.4.3 single 구문 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 15c180cd-e462-4b41-bf8c-cb8b1afb1a9b
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 81abf5324c215b9011ecbd774626a213c2eda653
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46376502"
---
# <a name="243-single-construct"></a>2.4.3 single 구문

합니다 **단일** 지시문 연결된 된 구조화 된 블록 (반드시 마스터 스레드) 팀에서 하나의 스레드에 의해 실행 되도록 지정 하는 구문으로 식별 합니다. 구문의 합니다 **단일** 지시문은 다음과 같습니다.

```
#pragma omp single [clause[[,] clause] ...] new-linestructured-block
```

절은 다음 중 하나입니다.

**private(** *variable-list* **)**

**firstprivate(** *variable-list* **)**

**copyprivate (** *변수 목록* **)**

**nowait**

암시적 장벽 후는 **단일** 하지 않는 경우 생성할를 **nowait** 절을 지정 합니다.

에 대 한 제한 된 **단일** 지시문은 다음과 같습니다.

- 단일 **nowait** 절에 나타날 수 있습니다는 **단일** 지시문입니다.

- **copyprivate** 절을 사용할 수 있어야 합니다 **nowait** 절.

## <a name="cross-references"></a>교차 참조:

- **개인**, **firstprivate**, 및 **copyprivate** 절을 참조 하세요 [2.7.2 섹션](../../parallel/openmp/2-7-2-data-sharing-attribute-clauses.md) 25 페이지입니다.