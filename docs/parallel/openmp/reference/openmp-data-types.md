---
title: OpenMP 데이터 형식 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
dev_langs:
- C++
ms.assetid: cf1e1045-4d12-4d03-80b7-d5843b80ef85
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: b41eaf7012c1d119071281f98177e4a4d841890b
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46410075"
---
# <a name="openmp-data-types"></a>OpenMP 데이터 형식

OpenMP API에서 사용 되는 데이터 형식에 대 한 링크를 제공 합니다.

표준 OpenMP의 Visual c + + 구현에는 다음 데이터 형식 포함 됩니다.

|데이터 형식|설명|
|---------------|-----------------|
|[omp_lock_t](../../../parallel/openmp/reference/omp-lock-t.md)|잠금, 잠금을 사용할 수 있는지 또는 스레드가 잠금을 소유 하는 경우의 상태를 보유 하는 형식입니다.|
|[omp_nest_lock_t](../../../parallel/openmp/reference/omp-nest-lock-t.md)|잠금에 대 한 정보는 다음과 같은 부분 중 하나를 포함 하는 형식: 잠금을 사용할 수는 스레드의 id를 소유 하는 잠금 및 중첩 수 있는지 여부를 합니다.|

## <a name="see-also"></a>참고 항목

[라이브러리 참조](../../../parallel/openmp/reference/openmp-library-reference.md)