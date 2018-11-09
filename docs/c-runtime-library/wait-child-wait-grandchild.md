---
title: _WAIT_CHILD, _WAIT_GRANDCHILD
ms.date: 11/04/2016
f1_keywords:
- _WAIT_GRANDCHILD
- WAIT_CHILD
- WAIT_GRANDCHILD
- _WAIT_CHILD
helpviewer_keywords:
- WAIT_CHILD constant
- WAIT_GRANDCHILD constant
- _WAIT_CHILD constant
- _WAIT_GRANDCHILD constant
ms.assetid: 7acd96fa-d118-4339-bb00-e5afaf286945
ms.openlocfilehash: 50519ffe8e2de784a9596a1dc748741bbd4cd278
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50613956"
---
# <a name="waitchild-waitgrandchild"></a>_WAIT_CHILD, _WAIT_GRANDCHILD

## <a name="syntax"></a>구문

```

#include <process.h>

```

## <a name="remarks"></a>설명

`_cwait` 함수는 다른 프로세스를 대기하는 모든 프로세스에서 사용할 수 있습니다(프로세스 ID가 알려진 경우). 작업 인수는 다음 값 중 하나가 될 수 있습니다.

|상수|의미|
|--------------|-------------|
|`_WAIT_CHILD`|호출 프로세스는 지정된 새 프로세스가 종료될 때까지 대기합니다.|
|`_WAIT_GRANDCHILD`|호출 프로세스는 지정된 새 프로세스 및 해당 새 프로세스에 의해 생성된 모든 프로세스가 종료될 때까지 대기합니다.|

## <a name="see-also"></a>참고 항목

[_cwait](../c-runtime-library/reference/cwait.md)<br/>
[전역 상수](../c-runtime-library/global-constants.md)