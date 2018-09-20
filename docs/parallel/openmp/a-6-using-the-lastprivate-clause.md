---
title: A.6 lastprivate 절 사용 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: cf3bf0cc-aa46-4e44-9433-e2969e3be2c1
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 03d18d3aaf5c5d1cbe03282710ae4f4e2bb613f3
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46390581"
---
# <a name="a6---using-the-lastprivate-clause"></a>A.6   lastprivate 절 사용

경우에 따라 올바른 실행 루프의 마지막 반복을 변수에 할당 되는 값에 따라 달라 집니다. 이러한 프로그램에 대 한 인수로 이러한 모든 변수를 나열 해야 합니다는 `lastprivate` 절 ([2.7.2.3 섹션](../../parallel/openmp/2-7-2-3-lastprivate.md) 27 페이지) 되도록 변수의 값은 루프가 순차적으로 실행 될 때와 동일 합니다.

```
#pragma omp parallel
{
   #pragma omp for lastprivate(i)
      for (i=0; i<n-1; i++)
         a[i] = b[i] + b[i+1];
}
a[i]=b[i];
```

이전 예제에서는 변수의 `i` 병렬 영역의 끝은 같습니다 `n-1`, 순차적 경우에서.