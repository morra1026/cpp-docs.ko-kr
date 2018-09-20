---
title: 2.2 조 건 부 컴파일 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 8f9c914d-736c-48cf-899d-c8029dbe1e32
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 25b52ce624777efe85e27b8ce5e7941bc2f5dcba
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46440383"
---
# <a name="22-conditional-compilation"></a>2.2 조건부 컴파일

_**OPENMP** 10 진 상수와 매크로 이름이 OpenMP 규격 구현에서 정의 된 *yyyymm*, 연도 및 월의 승인 된 사양을 수 있습니다. 이 매크로는의 주체를 사용 해야 합니다.는 **#define** 또는 **#undef** 전처리 지시문입니다.

```
#ifdef _OPENMP
iam = omp_get_thread_num() + index;
#endif
```

공급 업체 확장 openmp를 정의 하는 경우 추가 미리 정의 된 매크로 지정할 수 있습니다.