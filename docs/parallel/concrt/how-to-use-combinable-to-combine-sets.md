---
title: '방법: combinable 집합 결합을 사용 하 여 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-concrt
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- combinable class, example
- combining sets with combinable [Concurrency Runtime]
ms.assetid: 66ffe8e3-6bbb-4e9f-b790-b612922a68a7
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 69f48ed099fe033ba1847a3414ed8e5c5ce88f71
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46433675"
---
# <a name="how-to-use-combinable-to-combine-sets"></a>방법: combinable을 사용하여 집합 결합

이 항목에서는 사용 하는 [concurrency:: combinable](../../parallel/concrt/reference/combinable-class.md) 소수 집합을 계산 하는 클래스입니다.

## <a name="example"></a>예제

다음 예에서는 소수 집합을 두 번 계산합니다. 각 계산의 결과 저장 한 [std::bitset](../../standard-library/bitset-class.md) 개체입니다. 먼저 집합을 순차적으로 계산 하 고 집합을 병렬로 계산 합니다. 또한 이 예제에서는 두 계산을 모두 수행하는 데 필요한 시간을 콘솔에 출력합니다.

이 예제에서는 합니다 [concurrency:: parallel_for](reference/concurrency-namespace-functions.md#parallel_for) 알고리즘으로 `combinable` 스레드 로컬 집합을 생성 하는 개체입니다. 사용 하 여는 [concurrency::combinable::combine_each](reference/combinable-class.md#combine_each) 최종 집합에 스레드 로컬 집합을 결합 하는 방법입니다.

[!code-cpp[concrt-parallel-combine-primes#1](../../parallel/concrt/codesnippet/cpp/how-to-use-combinable-to-combine-sets_1.cpp)]

프로세서가 4개인 컴퓨터의 샘플 출력은 다음과 같습니다.

```Output
serial time: 312 ms

parallel time: 78 ms
```

## <a name="compiling-the-code"></a>코드 컴파일

예제 코드를 복사 하 고 Visual Studio 프로젝트에 붙여 넣습니다 또는 라는 파일에 붙여 `parallel-combine-primes.cpp` Visual Studio 명령 프롬프트 창에서 다음 명령을 실행 합니다.

**cl.exe /EHsc 병렬-결합-primes.cpp**

## <a name="see-also"></a>참고 항목

[병렬 컨테이너 및 개체](../../parallel/concrt/parallel-containers-and-objects.md)<br/>
[combinable 클래스](../../parallel/concrt/reference/combinable-class.md)<br/>
[combinable:: combine_each 메서드](reference/combinable-class.md#combine_each)

