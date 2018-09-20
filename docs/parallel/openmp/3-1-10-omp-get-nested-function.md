---
title: 3.1.10 omp_get_nested 함수 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 48736a25-5c6e-4e2d-aad0-421087663a3c
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: d019dd757080bbc87ff7aaab1a8745b2a3156b39
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46392283"
---
# <a name="3110-ompgetnested-function"></a>3.1.10 omp_get_nested 함수

`omp_get_nested` 비활성화 된 경우 함수는 중첩 된 병렬 처리를 사용 하는 경우 0이 아닌 값 및 0 반환 합니다. 중첩 된 병렬 처리에 대 한 자세한 내용은 40 페이지 3.1.9 섹션을 참조 하세요. 형식은 다음과 같습니다.

```
#include <omp.h>
int omp_get_nested(void);
```

구현에서 중첩 된 병렬 처리를 구현 하지 않으면,이 함수는 항상 0을 반환 합니다.