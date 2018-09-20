---
title: 2.7.2.8 copyprivate | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: c382348c-c785-45b2-8ee6-a66b76b97f3e
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 6815afe12344f94ed33d6b9260472f3e29eb72a0
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46406362"
---
# <a name="2728-copyprivate"></a>2.7.2.8 copyprivate

합니다 **copyprivate** 절 개인 변수를 사용 하 여 다른 구성원에 게 팀의 한 멤버에서 값을 브로드캐스트 메커니즘을 제공 합니다. 경우에 공유 변수를 제공 (예를 들어, 각 수준에서 서로 다른 변수를 요구 하는 재귀)에서 어려운 값에 대 한 공유 변수를 사용 하는 대신 것입니다. 합니다 **copyprivate** 절 에서만 나타날 수 있습니다 합니다 **단일** 지시문입니다.

구문의 합니다 **copyprivate** 절은 다음과 같습니다.

```

copyprivate(
variable-list
)

```

미치는 **copyprivate** 해당 변수 목록에서 변수에서 절을 연관 구조화 된 블록으로 실행 된 후 발생 합니다 **단일** 생성, 앞에 있는 스레드 중 하나는 팀이 해당 구문의 끝 장벽을 남았습니다. 그런 다음, 각 변수에 대 한 팀의 다른 모든 스레드는 *변수 목록*, 해당 변수가 정의한 (처럼 할당) 해당 값을 사용 하 여 구조적 구문을 실행 하는 스레드에서 변수 블록입니다.

에 대 한 제한 된 **copyprivate** 절은 다음과 같습니다.

- 에 지정 된 변수를 **copyprivate** 절에 나타나지 않아야는 **개인** 하거나 **firstprivate** 동일한 절 **단일**지시문입니다.

- 경우는 **단일** 지시문에 **copyprivate** 절 동적 병렬 영역 범위에서 발생 하면에 지정 된 모든 변수는 **copyprivate** 절 이어야 합니다 바깥쪽 컨텍스트에서 private.

- 에 지정 된 변수를 **copyprivate** 절에는 액세스할 수 있는 명확한 복사 할당 연산자는 있어야 합니다.