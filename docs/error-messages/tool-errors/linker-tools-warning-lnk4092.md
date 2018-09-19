---
title: 링커 도구 경고 LNK4092 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- LNK4092
dev_langs:
- C++
helpviewer_keywords:
- LNK4092
ms.assetid: d569ec47-a338-40e1-940b-8a8061459acb
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b9b47b347e11e640425bc7840a0f78a33e9e3b7e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46113424"
---
# <a name="linker-tools-warning-lnk4092"></a>링커 도구 경고 LNK4092

쓰기 가능한 공유 섹션 'section'에 재배치가 있습니다. 이미지가 올바르게 실행 되지 않을 수 있습니다.

링커는 잠재적으로 심각한 문제가 경고 메시지를 공유 섹션과 있을 때마다이 경고를 내보냅니다.

섹션을 "공유 합니다."로 표시 하는 여러 프로세스 간에 데이터를 공유 하는 한 가지 방법은 그러나 공유 섹션과 표시 문제가 발생할 수 있습니다. 예를 들어, 공유 데이터 섹션에서 다음과 같은 선언이 포함 된 DLL 해야 합니다.

```
int var = 1;
int *pvar = &var;
```

링커를 확인할 수 없습니다 `pvar` 메모리에서 DLL이 로드 되는 위치에 해당 값에 따라 달라, 따라서 배치 재배치 레코드 DLL입니다. 메모리의 주소에 DLL이 로드 하는 경우 `var` 해결할 수 있습니다 및 `pvar` 할당 합니다. 다른 프로세스가 동일한 DLL을 로드 동시에 로드할 수 없는 경우 주소, 주소에 재배치 `var` 첫 번째 프로세스의 주소 공간과 두 번째 프로세스에서 잘못 된 주소를 가리킵니다 업데이트 됩니다.