---
title: 2.7.2.3 lastprivate
ms.date: 11/04/2016
ms.assetid: 77f6a5c9-704f-4a88-8476-29db852ed800
ms.openlocfilehash: 15f9af23c4f4e1c0ce2914a979f7a41e7b4a6bc1
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50428461"
---
# <a name="2723-lastprivate"></a>2.7.2.3 lastprivate

합니다 `lastprivate` 절에서 제공 하는 기능의 상위 집합을 제공 합니다 `private` 절. 구문의 `lastprivate` 절은 다음과 같습니다.

```
lastprivate(variable-list)
```

에 지정 된 변수를 *변수 목록* 가 `private` 절 의미 체계. 경우는 `lastprivate` 에서 작업 공유 구문에 각 값을 식별 하는 지시문의 절이 나타납니다 `lastprivate` 변수가 연결된 루프 또는 어휘 적으로 마지막 섹션 지시문을 순차적으로 마지막 반복에서 할당 되는 변수의 원본 개체입니다. 마지막 반복에서 값이 할당 되지 않은 변수를 **에 대 한** 또는 **에 대 한 병렬**, 또는 어휘 적으로 마지막 섹션을 **섹션** 또는  **섹션에서는 병렬** 지시문 구문 비활성화 상태 값 후 합니다. 할당 되지 않은 하위 개체는 구문이 후 비활성화 상태 값을 수도 있습니다.

제한 된 `lastprivate` 절은 다음과 같습니다.

- 에 대 한 모든 제한 `private` 적용 합니다.

- 으로 지정 된 클래스 형식의 변수에 `lastprivate` 액세스 가능 하며 명확한 복사 할당 연산자가 있어야 합니다.

- 병렬 영역 내부에서는 개인 기능은에 나타나는 변수를 `reduction` 절을 **병렬** 지시문에 지정할 수는 `lastprivate` 병렬 구문에 바인딩하는 작업 공유 지시문의 절.