---
title: 3.1.8 omp_get_dynamic 함수 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: c03e2daf-29c9-49e3-9b67-b980ad1ab195
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 2c30f49eaf91353d6a7cd9bd26e0e10e95cb6acd
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46426785"
---
# <a name="318-ompgetdynamic-function"></a>3.1.8 omp_get_dynamic 함수

합니다 **omp_get_dynamic** 스레드를 동적으로 조정 사용 하 고 그렇지 않으면 0을 반환 하는 경우 함수는 0이 아닌 값을 반환 합니다. 형식은 다음과 같습니다.

```
#include <omp.h>
int omp_get_dynamic(void);
```

구현에는 스레드 수를 동적으로 조정 구현 하지 않으면,이 함수는 항상 0을 반환 합니다.

## <a name="cross-references"></a>교차 참조:

- 동적 스레드 조정에 대 한 참조 [3.1.7 섹션](../../parallel/openmp/3-1-7-omp-set-dynamic-function.md) 39 페이지입니다.