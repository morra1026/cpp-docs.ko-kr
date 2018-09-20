---
title: 2.6.3 barrier 지시문 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 4485a3d7-533f-4fec-8128-a131bec7fa16
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 8654534143e6feed06e93406c8fe03983ee9c2fc
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46429151"
---
# <a name="263-barrier-directive"></a>2.6.3 barrier 지시문

합니다 **장벽** 지시문 팀의 모든 스레드를 동기화 합니다. 발생 하면 팀의 각 스레드가 다른 모든 것이 점에 도달할 때까지 기다립니다. 구문의 합니다 **장벽** 지시문은 다음과 같습니다.

```
#pragma omp barrier new-line
```

팀의 모든 스레드가 장애물, 발생 한 후 팀에서 각 스레드는 병렬에서 barrier 지시문 다음 문을 실행을 시작 합니다. 되므로 합니다 **장벽** 지시문에는 해당 구문의 일부로 C 언어 문이 없는, 프로그램에서의 위치에 몇 가지 제한이 있습니다. 참조 [부록 C](../../parallel/openmp/c-openmp-c-and-cpp-grammar.md) 정식 문법에 대 한 합니다. 아래 예제에서는 이러한 제한 사항을 보여 줍니다.

```
/* ERROR - The barrier directive cannot be the immediate
*          substatement of an if statement
*/
if (x!=0)
   #pragma omp barrier
...

/* OK - The barrier directive is enclosed in a
*      compound statement.
*/
if (x!=0) {
   #pragma omp barrier
}
```