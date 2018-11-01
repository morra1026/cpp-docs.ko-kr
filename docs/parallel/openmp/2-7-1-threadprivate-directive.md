---
title: 2.7.1 threadprivate 지시문
ms.date: 11/04/2016
ms.assetid: 08e0b70f-5359-4607-b0ca-38c2d570d7b3
ms.openlocfilehash: 0ba5ea4892d70458f0f63bcb5b92968b36235273
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50647007"
---
# <a name="271-threadprivate-directive"></a>2.7.1 threadprivate 지시문

`threadprivate` 명명 된 파일 범위, 네임 스페이스 범위, 또는 정적 블록 범위 변수에서 지정 된 지시문을 사용 하면 합니다 *변수 목록* 전용 스레드입니다. *변수 목록* 은 불완전 한 형식 없는 변수의 쉼표로 구분 된 목록입니다. 구문의 `threadprivate` 지시문은 다음과 같습니다.

```
#pragma omp threadprivate(variable-list) new-line
```

각 복사본을 `threadprivate` 변수가 초기화 한 번 해당 복사본에 대 한 첫 번째 참조 하기 전에 프로그램에서 일반적인 방식으로 지정 되지 않은 시점 (즉, 대로 직렬 실행 프로그램의 마스터 복사본을 초기화할 수는). 개체의 명시적 이니셜라이저에서 참조할 경우는 `threadprivate` 변수와 개체의 값은 변수의 복사본에 대 한 첫 번째 참조 하기 전에 수정 될 다음 동작이 지정 되지 않습니다.

모든 개인 변수를 사용 하 여 스레드가 다른 스레드의 복사본 참조 하지 않아야 하는 대로 `threadprivate` 개체입니다. 직렬 지역 및 프로그램의 마스터 지역 중 개체의 마스터 스레드 복사본 참조 됩니다.

첫 번째 병렬 지역을 실행 한 후의 데이터는 `threadprivate` 개체 동적 스레드 메커니즘 경우 비활성화 된만 사용 하며 모든 병렬 영역에 대 한 스레드 수를 그대로 유지 하도록 보장 됩니다.

제한 된 `threadprivate` 지시문은 다음과 같습니다.

- `threadprivate` 지시문 파일 범위 또는 네임 스페이스 범위 변수에 대 한 모든 정의 또는 선언, 외부 나타나야 하며 앞에 변수 중 하나에 대 한 모든 참조 목록에서 어휘와 야 합니다.

- 각 변수에 *변수 목록* 의 `threadprivate` 어휘 지시문 앞에 있는 파일이 나 네임 스페이스 범위에서 변수 선언에 지시문 파일이 나 네임 스페이스 범위에서 참조 해야 합니다.

- `threadprivate` 변수의 범위에 중첩된 된 범위에 없는 고정 블록 범위 변수에 대 한 지시문이 나타나야 합니다. 지시문 목록에 변수 중 하나에 대 한 모든 참조 앞에 어휘 적으로 해야 합니다.

- 각 변수에 *변수 목록* 의 `threadprivate` 어휘 지시문 앞에 있는 동일한 범위에서 변수 선언에 지시문 블록 범위에서 참조 해야 합니다. 변수 선언에는 정적 저장소 클래스 지정자를 사용 해야 합니다.

- 변수에서 지정 된 경우는 `threadprivate` 하나의 변환 단위에서 지시문이 지정 해야 합니다는 `threadprivate` 선언 되는 각 변환 단위에서 지시문입니다.

- `threadprivate` 변수를 제외한 모든 절에 나타나지 않아야 합니다 `copyin`, `copyprivate`, `schedule`를 `num_threads`, 또는 **경우** 절.

- 주소는 `threadprivate` 변수 주소 상수를 아닙니다.

- `threadprivate` 불완전 한 형식 이거나 참조 형식 변수 없어야 합니다.

- `threadprivate` 비 POD 클래스 형식의 변수에 명시적 이니셜라이저를 사용 하 여 선언 된 액세스 가능 하며 명확한 복사 생성자가 있어야 합니다.

다음 예제에서는 어떻게 이니셜라이저에 표시 되는 변수를 수정 하면 알 수 없는 동작 및 보조 개체 및 복사 생성자를 사용 하 여이 문제를 방지 하는 방법을 보여 줍니다.

```
int x = 1;
T a(x);
const T b_aux(x); /* Capture value of x = 1 */
T b(b_aux);
#pragma omp threadprivate(a, b)

void f(int n) {
   x++;
   #pragma omp parallel for
   /* In each thread:
   * Object a is constructed from x (with value 1 or 2?)
   * Object b is copy-constructed from b_aux
   */
   for (int i=0; i<n; i++) {
      g(a, b); /* Value of a is unspecified. */
   }
}
```

## <a name="cross-references"></a>교차 참조:

- 동적 스레드를 참조 하세요 [3.1.7 섹션](../../parallel/openmp/3-1-7-omp-set-dynamic-function.md) 39 페이지입니다.

- `OMP_DYNAMIC` 환경 변수를 참조 하십시오 [섹션 4.3](../../parallel/openmp/4-3-omp-dynamic.md) 49 페이지입니다.