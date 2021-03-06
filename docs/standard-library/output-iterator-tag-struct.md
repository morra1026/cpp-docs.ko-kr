---
title: output_iterator_tag 구조체
ms.date: 11/04/2016
f1_keywords:
- xutility/std::output_iterator_tag
helpviewer_keywords:
- output_iterator_tag class
- output_iterator_tag struct
ms.assetid: c23a4331-b069-4fa0-9c3a-1c9be7095553
ms.openlocfilehash: cb2a59d2c81e6d7cc80de2714ba86476c5fa837f
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50659310"
---
# <a name="outputiteratortag-struct"></a>output_iterator_tag 구조체

에 대 한 반환 형식을 제공 하는 클래스 `iterator_category` 출력 반복기를 나타내는 함수입니다.

## <a name="syntax"></a>구문

output_iterator_tag 구조체 {};

## <a name="remarks"></a>설명

범주 태그 클래스는 알고리즘 선택을 위한 컴파일 태그로 사용됩니다. 템플릿 함수는 컴파일 시간에서 가장 효율적인 알고리즘을 사용할 수 있도록 해당 반복기 인수의 가장 구체적인 범주를 찾아야 합니다. `Iterator` 형식의 모든 반복기에 대해 `iterator_traits`< `Iterator`> **::iterator_category**는 반복기 동작을 설명하는 가장 구체적인 범주 태그로 정의되어야 합니다.

형식은 동일 **반복기** \< **Iter**> **:: iterator_category** 때 `Iter` 으로 사용할 수 있는 개체에 설명 합니다.는 출력 반복기입니다.

이 태그는 다른 반복기 태그처럼 반복기에 대해 `value_type` 또는 `difference_type`에서 매개 변수화되지 않습니다. 출력 반복기에는 `value_type` 또는 `difference_type`이 없기 때문입니다.

## <a name="example"></a>예제

참조 [iterator_traits](../standard-library/iterator-traits-struct.md) 하거나 [random_access_iterator_tag](../standard-library/random-access-iterator-tag-struct.md) 사용 하는 방법의 예 `iterator_tag`s입니다.

## <a name="requirements"></a>요구 사항

**헤더:** \<iterator>

**네임스페이스:** std

## <a name="see-also"></a>참고자료

[C++ 표준 라이브러리의 스레드 보안](../standard-library/thread-safety-in-the-cpp-standard-library.md)<br/>
[C++ 표준 라이브러리 참조](../standard-library/cpp-standard-library-reference.md)<br/>
