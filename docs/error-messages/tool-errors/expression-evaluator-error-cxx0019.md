---
title: 식 계산기 오류 CXX0019 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- CXX0019
dev_langs:
- C++
helpviewer_keywords:
- CXX0019
- CAN0019
ms.assetid: 4c6431fd-3310-4a61-934d-58b070b330fe
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 9f1e78bd88f35240e90332ef9a9139558051cab5
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50070129"
---
# <a name="expression-evaluator-error-cxx0019"></a>식 계산기 오류 CXX0019

잘못 된 형식 캐스팅

C 식 계산기 작성 하는 대로 형식 변환을 수행할 수 없습니다.

이 오류는 can0019와 동일 합니다.

### <a name="to-fix-by-checking-the-following-possible-causes"></a>다음과 같은 가능한 원인을 확인하여 수정하려면

1. 지정된 된 형식을 알려진 아닙니다.

1. 포인터 형식의 수준이 너무 많아 있었습니다. 예를 들어, 유형 변환

    ```
    (char **)h_message
    ```

   C 식 계산기에서 계산할 수 없습니다.