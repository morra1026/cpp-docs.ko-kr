---
title: 3.3 타이밍 루틴 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 21060d64-cbe8-4e38-8718-3a68d6a57be3
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 8c9eda9ac8f60e66c8c4168d734bcf4459b0b63e
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46403983"
---
# <a name="33-timing-routines"></a>3.3 타이밍 루틴

이 섹션에서 설명 하는 기능은 이식 가능한 벽 시계 타이머를 지원 합니다.

- `omp_get_wtime` 함수 경과 된 벽 시계 시간을 반환 합니다.

- `omp_get_wtick` 연속 클록 틱 간 시간 (초)을 반환 합니다.