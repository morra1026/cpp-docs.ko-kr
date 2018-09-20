---
title: 2.6.6 ordered 구문 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 5b3c1ba5-cfb8-4b05-865b-f446ae1c9f7c
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 7b83c3dfc13b231a1314343a1dff496acf7a99b6
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46412199"
---
# <a name="266-ordered-construct"></a>2.6.6 ordered 구문

구조화 된 블록 다음을 **정렬** 지시문 순차 루프에서 반복 실행할 수는 있는 순서 대로 실행 됩니다. 구문의 합니다 **정렬** 지시문은 다음과 같습니다.

```
#pragma omp ordered new-linestructured-block
```

**정렬** 지시문의 동적 범위 내에 있어야 합니다.를 **에 대 한** 하거나 **에 대 한 병렬** 생성 합니다. **에 대 한** 또는 **에 대 한 병렬** 는 지시문을 **정렬** 구문을 바인딩합니다 있어야는 **정렬** 에 설명 된 대로 지정 된 절 [2.4.1 섹션](../../parallel/openmp/2-4-1-for-construct.md) 11 페이지입니다. 실행에서을 **에 대 한** 또는 **에 대 한 병렬** 사용 하 여 생성는 **정렬** 절 **정렬** 구문에 엄격 하 게 실행 되는 이러한는 실행할 수 있는 순차 루프 실행에서 순서입니다.

에 대 한 제한 합니다 **정렬** 지시문은 다음과 같습니다.

- 사용 하는 루프의 반복을 **에 대 한** 구문이 동일한 순서가 지정 된 지시문을 두 번 이상 실행 해서는 안을 둘 이상 실행 하지 해야 **정렬** 지시문입니다.