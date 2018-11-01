---
title: 2.6.1 master 구문
ms.date: 11/04/2016
ms.assetid: c092064b-ea57-4d4e-9c99-a004d65656fe
ms.openlocfilehash: 0501b1fdfbd36829cee2793fc0f7bb03daeda900
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50475532"
---
# <a name="261-master-construct"></a>2.6.1 master 구문

합니다 **마스터** 지시문 팀의 마스터 스레드에 의해 실행 되는 구조화 된 블록을 지정 하는 구문으로 식별 합니다. 구문의 합니다 **마스터** 지시문은 다음과 같습니다.

```
#pragma omp master new-linestructured-block
```

팀의 다른 스레드에 연결된 된 구조화 된 블록을 실행 하지 마십시오. 항목 또는 종료 master 구문에서 암시적된 장벽이 없습니다 있습니다.