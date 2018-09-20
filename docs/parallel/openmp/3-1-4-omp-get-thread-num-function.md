---
title: 3.1.4 omp_get_thread_num 함수 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 5220402b-c109-4b1f-ba79-002e93d08617
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 5a21a682c051daffde16b3d5cfc63fd2d679c4de
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46444920"
---
# <a name="314-ompgetthreadnum-function"></a>3.1.4 omp_get_thread_num 함수

`omp_get_thread_num` 함수를 실행 하는 스레드의 해당 팀 내에서 스레드 수를 반환 합니다. 스레드 번호 힘은 0 및 **omp_get_num_threads()**-1을 포함 합니다. 팀의 마스터 스레드는 스레드 0입니다.

형식은 다음과 같습니다.

```
#include <omp.h>
int omp_get_thread_num(void);
```

직렬 지역에서 호출 된 경우 `omp_get_thread_num` 0을 반환 합니다. Serialize 되는 중첩 된 병렬 영역 내부에서 호출 하는 경우이 함수는 0을 반환 합니다.

## <a name="cross-references"></a>교차 참조:

- `omp_get_num_threads` 함수를 참조 하세요 [단원 3.1.2](../../parallel/openmp/3-1-2-omp-get-num-threads-function.md) 37 페이지입니다.