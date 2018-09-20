---
title: 4.4 OMP_NESTED | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: fd17b6f4-84e8-44c0-a96a-3a9e5ba33688
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 1083269f31ebc710da24430635ff8381e3f2147a
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46419518"
---
# <a name="44-ompnested"></a>4.4 OMP_NESTED

합니다 `OMP_NESTED` 환경 변수 사용 하거나 중첩 된 병렬 처리는 사용 하도록 설정 하거나 호출 하 여 사용 하지 않도록 설정 하지 않는 한 중첩 된 병렬 처리를 사용 하지 않도록 설정 합니다 `o` **mp_set_nested** 라이브러리 루틴입니다. 경우로 **TRUE**, 중첩 된 병렬 처리로 설정 된 경우 사용 되 **FALSE**중첩 된 병렬 처리를 사용 하지 않도록 설정 합니다. 기본값은 **FALSE**합니다.

예제:

```
setenv OMP_NESTED TRUE
```

## <a name="cross-reference"></a>상호 참조를 삽입 합니다.

- `omp_set_nested` 함수를 참조 하세요 [3.1.9 섹션](../../parallel/openmp/3-1-9-omp-set-nested-function.md) 40 페이지입니다.