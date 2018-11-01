---
title: '방법: Alloc 및 Free를 사용하여 메모리 성능 개선'
ms.date: 11/04/2016
helpviewer_keywords:
- Alloc and Free, using [Concurrency Runtime]
- Using Alloc and Free [Concurrency Runtime]
ms.assetid: e1fab9e8-a97d-4104-bead-e95958db79f9
ms.openlocfilehash: d91734859cd7d3499979566f427c10a0f026941b
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50467823"
---
# <a name="how-to-use-alloc-and-free-to-improve-memory-performance"></a>방법: Alloc 및 Free를 사용하여 메모리 성능 개선

이 문서에서는 사용 하는 방법을 보여 줍니다.는 [concurrency:: alloc](reference/concurrency-namespace-functions.md#alloc) 하 고 [concurrency:: free](reference/concurrency-namespace-functions.md#free) 메모리 성능을 향상 시키는 함수입니다. 세 가지 다른 형식에 대 한 병렬 배열 요소의 반대로 하는 데 필요한 시간을 비교 각각 지정 합니다 `new` 및 `delete` 연산자입니다.

`Alloc` 하 고 `Free` 함수는 둘 다는 여러 스레드가 자주 호출 하는 경우 가장 유용 `Alloc` 고 `Free`합니다. 런타임에서;는 각 스레드에 대해 별도 메모리 캐시를 보유합니다. 따라서 런타임에서 잠금이나 메모리 장벽을 사용 하지 않고 메모리를 관리 합니다.

## <a name="example"></a>예제

다음 예제에서는 세 가지 형식을 지정 하는 각 합니다 `new` 고 `delete` 연산자입니다. `new_delete` 클래스를 사용 하 여 전역 `new` 하 고 `delete` 연산자를 `malloc_free` 클래스 C 런타임을 사용 하 여 [malloc](../../c-runtime-library/reference/malloc.md) 및 [무료](../../c-runtime-library/reference/free.md) 함수 및 `Alloc_Free` 클래스에서는 동시성 런타임을 `Alloc` 및 `Free` 함수입니다.

[!code-cpp[concrt-allocators#1](../../parallel/concrt/codesnippet/cpp/how-to-use-alloc-and-free-to-improve-memory-performance_1.cpp)]

## <a name="example"></a>예제

다음 예제에서는 `swap` 및 `reverse_array` 함수를 보여 줍니다. `swap` 함수는 지정 된 인덱스 배열의 내용을 교환 합니다. 임시 변수 힙에서 메모리를 할당합니다. `reverse_array` 함수 대형 배열을 만들고 동시에 여러 번 배열의 하는 데 필요한 시간을 계산 합니다.

[!code-cpp[concrt-allocators#2](../../parallel/concrt/codesnippet/cpp/how-to-use-alloc-and-free-to-improve-memory-performance_2.cpp)]

## <a name="example"></a>예제

다음 예제와 `wmain` 함수에 필요한 시간을 계산 하는 합니다 `reverse_array` 작업할 함수는 `new_delete`, `malloc_free`, 및 `Alloc_Free` 다른 메모리 할당 체계를 사용 하 여 각 형식.

[!code-cpp[concrt-allocators#3](../../parallel/concrt/codesnippet/cpp/how-to-use-alloc-and-free-to-improve-memory-performance_3.cpp)]

## <a name="example"></a>예제

전체 예제를 따릅니다.

[!code-cpp[concrt-allocators#4](../../parallel/concrt/codesnippet/cpp/how-to-use-alloc-and-free-to-improve-memory-performance_4.cpp)]

이 예에서는 4 개의 프로세서가 있는 컴퓨터에 대 한 다음 샘플 출력을 생성 합니다.

```Output
Took 2031 ms with new/delete.
Took 1672 ms with malloc/free.
Took 656 ms with Alloc/Free.
```

이 예에서 사용 하는 형식의 `Alloc` 하 고 `Free` 함수 때문에 메모리 성능을 높일 수는 `Alloc` 및 `Free` 자주 할당 및 여러에서 메모리 블록을 해제에 대 한 최적화 된 함수 스레드입니다.

## <a name="compiling-the-code"></a>코드 컴파일

예제 코드를 복사 하 고 Visual Studio 프로젝트에 붙여 넣습니다 또는 라는 파일에 붙여 `allocators.cpp` Visual Studio 명령 프롬프트 창에서 다음 명령을 실행 합니다.

**cl.exe /EHsc allocators.cpp**

## <a name="see-also"></a>참고 항목

[메모리 관리 함수](../../parallel/concrt/memory-management-functions.md)<br/>
[Alloc 함수](reference/concurrency-namespace-functions.md#alloc)<br/>
[Free 함수](reference/concurrency-namespace-functions.md#free)

