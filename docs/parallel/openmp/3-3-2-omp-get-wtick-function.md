---
title: 3.3.2 omp_get_wtick 함수 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 1ad08500-bcb0-40d9-a81f-f131819006c9
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 0111e7ee1d4eba0a7ca9edf50d99cef8d052f6a1
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46380318"
---
# <a name="332-ompgetwtick-function"></a>3.3.2 omp_get_wtick 함수

`omp_get_wtick` 반환 배정밀도 부동 소수점 값 시간 (초) 수와 같은 연속 클록 틱 간입니다. 형식은 다음과 같습니다.

```
#include <omp.h>
double omp_get_wtick(void);
```