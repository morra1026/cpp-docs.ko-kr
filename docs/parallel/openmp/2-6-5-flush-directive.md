---
title: 2.6.5 flush 지시문 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: a2ec5f74-9c37-424a-8376-47ab4a5829a2
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: d67453b636d50fcb78092318ebb76f5192817548
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46442736"
---
# <a name="265-flush-directive"></a>2.6.5 flush 지시문

합니다 **플러시** 지시문, 명시적 또는 묵시적 지정 구현이 필요 (아래)에 지정 하는 특정 개체의 일관 된 뷰를 팀의 모든 스레드에 있는지 확인 하는 "크로스 스레드" 시퀀스 위치 메모리입니다. 즉, 해당 개체를 참조 하는 식에 대 한 이전 평가 완료 하 고 후속 평가판이 아직 시작 되지 않은 합니다. 예를 들어, 컴파일러 메모리, 레지스터에서 개체의 값에 복원 해야 및 하드웨어 쓰기 버퍼 메모리를 플러시하고 메모리에서 개체의 값을 다시 로드 해야 할 수 있습니다.

구문의 합니다 **플러시** 지시문은 다음과 같습니다.

```
#pragma omp flush [(variable-list)]  new-line
```

동기화가 필요한 개체 모두 지정할 수 있습니다 변수인 경우 선택 사항인 이러한 변수를 지정할 수 있습니다 *변수 목록*합니다. 에 대 한 포인터 있으면 합니다 *변수 목록*포인터 자체 플러시, 개체가 아닌 포인터를 참조 합니다.

A **플러시** 없이 지시문을 *변수 목록* 자동 저장 기간이 있는 액세스할 수 없는 개체를 제외 하 고 모든 공유 개체를 동기화 합니다. (이 경우 보다 더 많은 오버 헤드가 발생할 수 있습니다는 **플러시** 사용 하 여를 *변수 목록*.) A **플러시** 없이 지시문을 *변수 목록* 다음 지시문 것을 의미:

- `barrier`

- 항목 및 종료 **중요**

- 항목 및 종료 `ordered`

- 항목 및 종료 **병렬**

- At에서 종료 **에 대 한**

- At에서 종료 **섹션**

- At에서 종료 **단일**

- 항목 및 종료 **에 대 한 병렬**

- 항목 및 종료 **병렬 섹션**

경우 지시문은 암시 되지 않습니다는 `nowait` 절이 있습니다. 유의 해야 하는 **플러시** 지시문은 다음 중 하나에 대 한 암시 되지 않습니다:

- 항목에서 **에 대 한**

- 항목 또는 종료 **마스터**

- 항목에서 **섹션**

- 항목에서 **단일**

Volatile 한정 형식의 개체의 값에 액세스 하는 참조 처럼 동작을 **플러시** 이전 시퀀스 지점에서 해당 개체를 지정 하는 지시문입니다. Volatile 한정 형식의 개체의 값을 수정 하는 참조 처럼 동작 하는 **플러시** 후속 시퀀스 위치에서 해당 개체를 지정 하는 지시문입니다.

되므로 합니다 **플러시** 지시문에는 해당 구문의 일부로 C 언어 문이 없는, 프로그램에서의 위치에 몇 가지 제한이 있습니다. 참조 [부록 C](../../parallel/openmp/c-openmp-c-and-cpp-grammar.md) 정식 문법에 대 한 합니다. 아래 예제에서는 이러한 제한 사항을 보여 줍니다.

```
/* ERROR - The flush directive cannot be the immediate
*          substatement of an if statement.
*/
if (x!=0)
   #pragma omp flush (x)
...

/* OK - The flush directive is enclosed in a
*      compound statement
*/
if (x!=0) {
   #pragma omp flush (x)
}
```

에 대 한 제한 된 **플러시** 지시문은 다음과 같습니다.

- 에 지정 된 변수를 **플러시** 지시문 참조 형식에 없어야 합니다.