---
title: 2.6.2 critical 구문 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: c46ecd00-b4a2-4a5e-ba92-288c329e773a
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: e51bd425999081c7a06a7d5692dbea16c887fa0b
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46417854"
---
# <a name="262-critical-construct"></a>2.6.2 critical 구문

합니다 **중요 한** 지시문 식별 한 번에 단일 스레드에 연결된 된 구조화 된 블록 실행을 제한 하는 구문입니다. 구문의 합니다 **중요 한** 지시문은 다음과 같습니다.

```
#pragma omp critical [(name)]  new-linestructured-block
```

선택적인 *이름을* 중요 영역을 식별할 수 있습니다. 중요 영역을 식별 하는 데 식별자 외부 링크가 있으며 레이블, 태그, 멤버 및 일반 식별자에서 사용 하는 네임 스페이스를 별도로 네임 스페이스입니다.

스레드가 다른 스레드가 동일한 이름 가진 (프로그램)에서 아무 곳 이나 중요 영역 실행 될 때까지 중요 영역 맨 앞에 대기 합니다. 모든 명명 되지 않은 **중요 한** 지시문 이름이 지정 되지 않은 매핑됩니다.