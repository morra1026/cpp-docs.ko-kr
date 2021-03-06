---
title: 1. 소개
ms.date: 01/16/2019
ms.assetid: c42e72bc-0e31-4b1c-b670-cd82673c0c5a
ms.openlocfilehash: 8c735408bdf9f9a13693bd0ad25df185bb1db42a
ms.sourcegitcommit: 382e247c0f1b4cb7c2dab837b8b6fdff24bff47a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/28/2019
ms.locfileid: "55087277"
---
# <a name="1-introduction"></a>1. 소개

이 문서는 컴파일러 지시문, 라이브러리 함수 및 C 및 c + + 프로그램에서 공유 메모리 병렬 처리를 지정 하는 데 사용할 수 있는 환경 변수 컬렉션을 지정 합니다. 이 문서에서 설명한 기능 이라고 통칭 합니다 *OpenMP C/c + + 응용 프로그램 인터페이스 (API)* 합니다. 이 사양의 목적은 모델을 제공 하는 병렬 프로그래밍에 대 한 여러 공급 업체에서 공유 메모리 아키텍처 간에 이식 가능 하도록 프로그램을 허용 합니다. 대부분의 공급 업체에서 컴파일러는 OpenMP C/c + + API를 지원합니다. OpenMP에 대 한 자세한 내용은 포함 하 여는 *OpenMP Fortran 응용 프로그램 인터페이스*, 다음 웹 사이트에서 확인할 수 있습니다.

[https://www.openmp.org](https://www.openmp.org)

지시문, 라이브러리 함수 및이 문서에 정의 된 환경 변수 만들기 및 이식성을 허용 하는 동안 병렬 프로그램을 관리 할 수 있습니다. 지시문은 C 및 c + + 순차 프로그래밍 모델 (SPMD) 여러 데이터를 생성 하는 단일 프로그램, 작업 공유 구문 및 동기화 생성자를 사용 하 여 확장 합니다. 데이터의 개인화 하 고 공유도 지원합니다. OpenMP C 및 c + + API를 지 원하는 컴파일러 명령줄 옵션을 활성화 하 고 모든 OpenMP 컴파일러 지시문의 해석을 허용 하는 컴파일러를 포함 합니다.

## <a name="11-scope"></a>1.1 범위

이 사양은 컴파일러만 사용자 지향 병렬 처리를 여기서 명시적으로 정의 하는 작업을 포함 하 고 런타임 시스템 병렬에서 프로그램을 실행 하는 데 키를 누릅니다. 종속성, 충돌, 교착 상태, 경합 상태 또는 잘못 된 프로그램 실행에서 발생 하는 다른 문제를 확인 하는 데 필요한 OpenMP C 및 c + + 구현 하지 않습니다. OpenMP C 및 c + + API 구문을 사용 하 여 응용 프로그램을 올바르게 실행 되도록 책임이 있습니다. 컴파일러에서 생성 된 자동 병렬화 및 이러한 병렬 처리를 지원 하기 위해 컴파일러 지시문이이 문서에서 다루지 않습니다.

## <a name="12-definition-of-terms"></a>1.2 용어 정의

이 문서에서는 다음과 같은 용어가 사용 됩니다.

- barrier

  팀의 모든 스레드가 도달 해야 하는 동기화 지점입니다.  각 스레드는 팀의 모든 스레드가 시점에서 도착할 때까지 대기 합니다. 구현으로 생성 하는 암시적 barrier 지시문을 식별 하는 명시적 장벽이 있습니다.

- construct

  구문에는 문입니다. 지시문을 이루어져 구조화 된 블록이 옵니다. 일부 지시문 구문의 일부가 됩니다. (참조 *openmp 지시문* 에 [부록 C](c-openmp-c-and-cpp-grammar.md)).

- 지시문

  C 또는 c + + `#pragma` 뒤에 `omp` 식별자, 기타 텍스트 및 새 줄. 지시문은 프로그램 동작을 지정합니다.

- 동적 범위

  모든 문이 합니다 *어휘 범위*, 어휘 범위 내에서 문 실행 한 후의 결과로 실행 되는 함수 내에서 모든 문 또한 합니다. 동적 범위는 라고도 하는 *지역*합니다.

- 어휘 범위

  문 내에서 어휘 적으로 보유 한 *구조화 된 블록*합니다.

- 마스터 스레드

  팀을 만드는 스레드는 때를 *병렬 영역* 를 입력 합니다.

- 병렬 영역

  Parallel OpenMP를 바인딩하는 문을 생성 하 고 여러 스레드에서 실행 될 수 있습니다.

- private

  전용 변수 이름을 참조를 수행 하는 스레드를 고유한 저장소 블록을 지정 합니다. 개인 변수는 지정 하는 방법은 여러 가지가 있습니다: 병렬 영역 내부에서는 정의를 `threadprivate` 지시문을 `private`, `firstprivate`, `lastprivate`, 또는 `reduction` 절 또는 변수를 사용 하 여를 `for`루프 제어 변수를 `for` 바로 다음 루프를 `for` 또는 `parallel for` 지시문입니다.

- 지역

  동적 범위입니다.

- 직렬 지역

  에서만 실행 되는 문은 합니다 *스레드를 마스터* 의 동적 범위 외부 *병렬 영역*합니다.

- Serialize

  사용 하 여 병렬 구문을 실행 합니다.

  - 스레드는 단일 스레드만 (즉, 마스터 스레드는 병렬 구문에 대 한), 구성 된 팀

  - 직렬 (동일한 정렬 블록의 병렬 구문에 포함 되지 않은 것 처럼) 구조화 된 블록 내에서 문의 실행 순서 및

  - 반환 된 값에 영향을 주지 `omp_in_parallel()` (의 효과는 별도로 병렬 구문 중첩).

- 공유

  공유 변수는 단일 블록 저장소의 이름을 지정 합니다. 이 변수를 액세스 하는 팀의 모든 스레드가이 단일 저장소 블록을 액세스할 수도 있습니다.

- 구조화 된 블록

  구조화 된 블록에는 단일 항목 및 단일 종료 된 문 (단일 또는 복합)입니다. 문을 안팎으로 이동 하는 경우 해당 문에 구조화 된 블록. (이 규칙에 대 한 호출을 포함 `longjmp`(3 C) 또는 사용 `throw`있지만 호출 `exit` 허용 됩니다.) 열 때 항상 실행 시작 하는 경우 `{` 항상 닫는 끝나는 `}`, 복합 문은 구조화 된 블록입니다. 식, 선택 문, 반복 문 또는 `try` 블록은 해당 복합 문의로 묶어서 얻은 경우 구조화 된 블록 `{` 및 `}` 구조화 된 블록을 것입니다. 점프 문, labeled 문 또는 선언문 구조화 된 블록이 없습니다.

- 팀

  하나 이상의 스레드가 실행 구문의 협력 합니다.

- 스레드

  제어 흐름을 직렬, 일련의 개인 변수 및 공유 변수에 액세스할 수 있는 실행 엔터티.

- 변수

  개체를 이름을 지정 하는 필요에 따라 네임 스페이스 이름으로 정규화 된 식별자 합니다.

## <a name="13-execution-model"></a>1.3 실행 모델

OpenMP는 병렬 실행 분기-조인 모델을 사용합니다. 이 분기-조인 모델 하는 다양 한 문제를 해결 하는 데 유용 하지만 큰 배열 기반 응용 프로그램에 맞게 조정 됩니다. OpenMP 병렬 프로그램 (여러 스레드의 실행 및 전체 OpenMP 지원 라이브러리)으로 올바르게 실행 되는 프로그램을 지원 하기 위한 것입니다. 무시 지시문과 간단한 OpenMP 스텁 라이브러리를 올바르게 순차적으로 프로그램을 실행 하는 프로그램에 대 한 이기도 합니다. 그러나 가능 하 고 순차적으로 실행 하는 경우 올바르게 작동 하지 않습니다 하는 프로그램을 개발할 수 있습니다. 또한 다양 한 병렬 처리의 수치 연산 연결의 변경으로 인해 다른 숫자 결과 발생할 수 있습니다. 예를 들어, 직렬 추가 감소 추가 연결을 위한 병렬 영역 감소 보다 패턴이 있을 수 있습니다. 이러한 다양 한 연관성 부동 소수점 더하기의 결과 변경할 수 있습니다.

OpenMP C/c + + API를 사용 하 여 작성 된 프로그램 실행 이라는 단일 스레드로 실행을 시작 합니다 *스레드를 마스터*합니다. 마스터 스레드는 첫 번째 병렬 구문에 나올 때까지 직렬 지역에서 실행 합니다. OpenMP C/c + + api에서는 `parallel` 지시문에는 병렬 구문 구성 합니다. 병렬 구문 발생 하면 마스터 스레드가 스레드 팀을 만든 하 고 마스터는 팀의 마스터 됩니다. 팀에서 각 스레드에 작업 공유 생성자를 제외 하 고 병렬 영역의 동적 범위에서 문을 실행 합니다. 팀의 모든 스레드가 동일한 순서로 작업 공유 구문 발생 해야 하 고 스레드 중 하나 이상의 연결된 된 구조화 된 블록 내에서 문을 실행 합니다. 작업 공유 구문 없이 끝 묵시적 장벽은 `nowait` 절이 팀의 모든 스레드에 의해 실행 됩니다.

스레드는 공유 개체를 수정 하는 경우 실행 환경 뿐만 아니라 프로그램의 다른 스레드에 달라 집니다. 수정은 완료 되기를 다음 시퀀스 위치에서 다른 스레드의 관점에서 (에 정의 된 기본 언어) 개체는 volatile 일에 선언 된 경우에 보장 됩니다. 그렇지 않은 경우 수정 먼저 스레드 수정 후 완료 되도록 보장 됩니다. 다른 스레드가 다음 (또는 동시에) 참조를 `flush` (암시적 또는 명시적) 개체를 지정 하는 지시문입니다. 경우는 `flush` 부작용의 올바른 순서로 다른 OpenMP 지시문에 의해 포함 되는 지시문을 보장 하지 않습니다, 추가, 명시적 제공 해야 하는 프로그래머의 `flush` 지시문입니다.

병렬 구문의 완료 되 면 팀의 스레드는 암시적 장벽에 동기화 하 고 마스터 스레드만 실행을 계속 합니다. 한 프로그램에서 임의 개수의 병렬 구문 지정할 수 있습니다. 결과적으로, 프로그램 분기 및 실행 하는 동안 여러 번 조인 수 있습니다.

OpenMP C/c + + API 프로그래머가 병렬 구문 내에서 호출 된 함수에서 지시문을 사용할 수 있습니다. 어휘 범위의 병렬 구문에 나타나지 않지만 동적 범위 내에서 식별할 수 있습니다 하는 지시문 이라고 *분리 된* 지시문입니다. 분리 된 지시문을 사용 하 여 프로그래머에 게 동시에 최소한의 변경 내용만 순차적 프로그램을 사용 하 여 해당 프로그램의 주요 부분을 실행할 수 있습니다. 이 기능을 사용 하 여 병렬 프로그램 호출 트리의 최상위 수준 코드 수 있으며 지시문을 사용 하 여 호출된 된 함수 중 하나에서 실행을 제어할 수 있습니다.

C 및 c + +에 대 한 동기화 되지 않은 호출 출력 동일한 파일에 쓰는 함수는 비결 정적 순서에 다른 스레드에 의해 기록 된 데이터 표시 되는 출력에서 발생할 수 있습니다. 마찬가지로, 동일한 파일에서 읽는 함수에는 입력에 대 한 동기화 되지 않은 호출 확정적이 지 않은 순서로 데이터를 읽을 수 있습니다. I/o 동기화 되지 않은 사용 하 여 다른 파일에 액세스 하는 각 스레드는 I/O 함수는 직렬 실행 동일한 결과 생성 합니다.

## <a name="14-compliance"></a>1.4 규격

OpenMP C/c + + API의 구현은 *OpenMP 규격* 부록 3. 부록 A, B, D, E 및 F는 및 인식 하 고 화면에 보이는 대로 챕터 1, 2, 3, 4,이 사양의 모든 요소의 의미 체계를 유지 하는 경우 정보 목적 으로만 제공 되며 사양에 포함 되지 않습니다. API의 하위 집합만 포함 하는 구현을 OpenMP와 호환 되지 않습니다.

OpenMP C 및 c + + API 구현에서 지원 되는 기본 언어 확장입니다. 기본 언어는이 문서의 언어 구문 이나 표시 되는 확장을 지원 하지 않으면, OpenMP 구현 되지 않습니다 지원 해야 합니다.

모든 표준 C 및 c + + 라이브러리 함수 및 기본 제공 함수 (즉, 함수는 컴파일러에는 특정 기술 자료) 스레드로부터 안전 해야 합니다. 병렬 영역 내에서 서로 다른 스레드에 의해 스레드로부터 안전한 함수의 동기화 되지 않은 사용에는 정의 되지 않은 동작이 생성 하지 않습니다. 그러나 동작을 동일 하 게 직렬 지역 수 없습니다 수 있습니다. (임의의 숫자 생성 함수에는 예입니다.)

OpenMP C/c + + API 지정 동작은 특정 *구현 시 정의 합니다.* 표준에 맞는 OpenMP 구현 정의 하 고 이러한 경우 해당 동작을 문서에 필요 합니다. 구현 시 정의 된 동작의 목록을 참조 하세요 [부록 E](e-implementation-defined-behaviors-in-openmp-c-cpp.md)합니다.

## <a name="15-normative-references"></a>1.5 표준 참조

- ISO/IEC 9899:1999 *정보 기술-프로그래밍 언어-C*합니다. 이 OpenMP API 사양에서는 9899:1999 C99 라고 합니다.

- ISO/IEC 9899:1990 *정보 기술-프로그래밍 언어-C*합니다. 이 OpenMP API 사양에서는 ISO/IEC 9899:1990 C90 라고 합니다.

- ISO/IEC 14882:1998 *정보 기술-프로그래밍 언어-c + +* 합니다. 이 OpenMP API 사양 ISO/IEC 14882:1998 c + +로 가리킵니다.

이 OpenMP API 사양 C를 가리키는 경우 구현에서 지 원하는 기본 언어 참조가 됩니다.

## <a name="16-organization"></a>1.6 조직

- [런타임 라이브러리 함수](3-run-time-library-functions.md)
- [환경 변수](4-environment-variables.md)
- [구현 시 정의 된 동작에서 OpenMP C/c + +](e-implementation-defined-behaviors-in-openmp-c-cpp.md)
- [OpenMP C/c + +에서 버전 2.0의 새로운 기능](f-new-features-and-clarifications-in-version-2-0.md)
