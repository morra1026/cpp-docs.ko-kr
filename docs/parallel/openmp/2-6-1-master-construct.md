---
title: 2.6.1 master 구문 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: c092064b-ea57-4d4e-9c99-a004d65656fe
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 8d82ae673e428c635172f35f9b0f682aa65dc2b8
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46445635"
---
# <a name="261-master-construct"></a>2.6.1 master 구문

합니다 **마스터** 지시문 팀의 마스터 스레드에 의해 실행 되는 구조화 된 블록을 지정 하는 구문으로 식별 합니다. 구문의 합니다 **마스터** 지시문은 다음과 같습니다.

```
#pragma omp master new-linestructured-block
```

팀의 다른 스레드에 연결된 된 구조화 된 블록을 실행 하지 마십시오. 항목 또는 종료 master 구문에서 암시적된 장벽이 없습니다 있습니다.