---
title: 2.7.2.6 감소 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: e7630a15-2978-4dbe-a29b-3a46371a0151
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 05ed97968921692f69f2ff0040ae14dc41ef52b5
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46375604"
---
# <a name="2726-reduction"></a>2.7.2.6 reduction

이 절에 표시 되는 스칼라 변수에서 감소를 수행 *변수 목록*, 연산자로 *op*합니다. 구문의 `reduction` 절은 다음과 같습니다.

> reduction(*op*: *variable-list*)

감소는 다음 형식 중 하나를 사용 하 여 문에 대 한 일반적으로 지정 됩니다.

> *x* = *x* *op* *expr*
> *x* *binop* = *expr*
> *x* = *expr* *op* *x* (제외 빼기)에 대 한 *x*++
> ++*x*
> *x*--
> --*x*

다음은 각 문자에 대한 설명입니다.

*x*<br/>
에 지정 된 환산 변수 중 하나는 `list`합니다.

*variable-list*<br/>
스칼라 감소가 변수의 쉼표로 구분 된 목록입니다.

*expr*<br/>
참조 하지 않는 스칼라 형식이 있는 식을 *x*합니다.

*op*<br/>
Not 오버 로드 된 연산자는 하나만 +, &#42;,-, &amp;, ^, &#124;를 &amp; &amp;, 또는 &#124; &#124;.

*binop*<br/>
Not 오버 로드 된 연산자는 하나만 +, &#42;,-, &amp;, ^, 또는 &#124;합니다.

다음은의 예로 `reduction` 절:

```cpp
#pragma omp parallel for reduction(+: a, y) reduction(||: am)
for (i=0; i<n; i++) {
   a += b[i];
   y = sum(y, c[i]);
   am = am || b[i] == c[i];
}
```

예제와 같이 연산자는 함수 호출 내부 숨겨질 수 있습니다. 사용자는 연산자에 지정 된 주의 해야 합니다.는 `reduction` 절 감소 작업과 일치 합니다.

하지만의 오른쪽 피연산자는 &#124; &#124; 연산자 파생 작업이 없습니다.이 예제에 사용할 수 있지만 주의 해 서 사용 해야 합니다. 이 컨텍스트에서 루프의 순차 실행 하는 동안 발생할 수 없도록 보장 되는 부작용은 병렬 실행 하는 동안 발생할 수 있습니다. 이러한 차이 반복의 실행 순서는 확정적이 지 없기 때문에 발생할 수 있습니다.

연산자는 감소에 대 한 컴파일러에서 사용 된 모든 개인 변수의 초기 값을 확인 하 고 종료 연산자를 확인 하려면 사용 됩니다. 연산자를 명시적으로 지정 하면 감소 문을 구문 어휘 범위 외부에 있을 수 있습니다. 임의 개수의 `reduction` 지시문에 절을 지정할 수는 있지만 변수 하나만에 나타날 수 있습니다 `reduction` 지시문 절.

각 변수의 개인 복사본 *변수 목록* 만들어지면 각 스레드에 대해 하나 처럼는 `private` 절을 사용한 합니다. 개인 복사본 연산자에 따라 초기화 됩니다 (다음 표 참조).

영역의 끝을 `reduction` 절이 지정 되어, 원래 개체의 각 지정한 연산자를 사용 하 여 개인 복사본의 최종 값을 사용 하 여 원래 값을 조합한 결과 반영 하도록 업데이트 됩니다. 감소 연산자 (빼기), 제외 하 고 모든 연관 되며 컴파일러 계산 최종 값을 다시 연결 자유롭게 수 있습니다. (빼기 감소의 부분 결과 최종 값은 폼에 추가 됩니다.)

첫 번째 스레드가 포함 하는 절에 도달 하 고 감소 계산이 완료 될 때까지 유지 하도록 원래 개체의 값이 비활성화 됩니다.  일반적으로 계산; 구문의 끝에 완료 됩니다. 그러나 경우 합니다 `reduction` 절을 사용 하는 구문에서 `nowait` 는 적용 원래 개체의 값까지 결정 되지 않은 모든 스레드는 가완료되었는지에장벽동기화를수행한`reduction`절.

다음 표에서 사용할 수 있는 연산자 및 해당 정식 초기화 값을 나열 합니다. 실제 초기화 값을는 환산 변수 데이터 형식과 일치 됩니다.

|연산자|초기화|
|--------------|--------------------|
|+|0|
|&#42;|1|
|-|0|
|&amp;|~0|
|&#124;|0|
|^|0|
|&amp;&amp;|1|
|&#124;&#124;|0|

제한 된 `reduction` 절은 다음과 같습니다.

- 형식의 변수는 `reduction` 포인터 형식과 참조 형식은 허용 되지 않습니다 한다는 절 reduction 연산자에 대해 유효 해야 합니다.

- 에 지정 된 변수를 `reduction` 절이 아니어야 **const**-정규화 합니다.

- 병렬 영역 내부에서는 개인 기능은에 나타나는 변수를 `reduction` 절을 **병렬** 지시문에 지정할 수는 `reduction` 병렬 구문에 바인딩하는 작업 공유 지시문의 절.

   ```cpp
   #pragma omp parallel private(y)
   { /* ERROR - private variable y cannot be specified
                in a reduction clause */
      #pragma omp for reduction(+: y)
      for (i=0; i<n; i++)
         y += b[i];
   }

   /* ERROR - variable x cannot be specified in both
              a shared and a reduction clause */
   #pragma omp parallel for shared(x) reduction(+: x)
   ```
