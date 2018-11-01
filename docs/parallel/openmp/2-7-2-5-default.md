---
title: 2.7.2.5 기본값
ms.date: 11/04/2016
ms.assetid: c856df07-705c-4ad3-9105-a268dd33e939
ms.openlocfilehash: efb10913b74ebfae37c95d057955c87bdcfca9a7
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50580232"
---
# <a name="2725-default"></a>2.7.2.5 기본값

합니다 **기본** 절 변수의 데이터 공유 특성에 영향을 줄 수 있습니다. 구문의 합니다 **기본** 절은 다음과 같습니다.

```
default(shared | none)
```

지정 **default(shared)** 의 현재 표시 된 각 변수에 명시적으로 나열 하는 것과 같습니다는 **공유** 절 경우가 아니라면 **threadprivate** 또는 **단점**`t`-정규화 합니다. 명시적인 없으면 **기본** 절 기본 동작은 동일 경우 **default(shared)** 지정 되었습니다.

지정 **default (none)** 병렬 구문 어휘 범위에서 변수를 참조할 때마다 충족 해야 다음 중 하나 이상이 필요 합니다.

- 변수 참조를 포함 하는 구문의 데이터 공유 특성 절에 명시적으로 나열 됩니다.

- 변수는 병렬 구문 내에서 선언 됩니다.

- 변수가 **threadprivate**합니다.

- 변수가 한 **const**-형식을 정규화 합니다.

- 변수는에 대 한 루프 제어 변수를 **에 대 한** 바로 뒤에 오는 루프를 **에 대 한** 또는 **에 대 한 병렬** 루프 내에서 표시 하는 지시문 및 변수 참조 .

변수를 지정 하는 **firstprivate**를 **lastprivate**, 또는 **감소** 절 포함된 지시문을 바깥쪽 변수에 대 한 암시적 참조가 발생 컨텍스트입니다. 이러한 암시적 참조 위에 나열 된 요구 사항이 적용 됩니다.

단일 **기본** 절에서 지정할 수는 **병렬** 지시문입니다.

변수의 기본 데이터 공유 특성을 사용 하 여 재정의할 수 있습니다는 **사설**, **firstprivate**를 **lastprivate**, **감소**, 및 **공유** 다음 예제에서 볼 수 있듯이 절:

```
#pragma  omp  parallel  for  default(shared)  firstprivate(i)\
   private(x)  private(r)  lastprivate(i)
```