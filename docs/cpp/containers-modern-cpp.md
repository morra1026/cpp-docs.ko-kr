---
title: 컨테이너(모던 C++)
ms.date: 1/18/2018
ms.topic: conceptual
ms.openlocfilehash: 2da57bfca8b04f50a223dddfb886835c69f746a4
ms.sourcegitcommit: a1fad0a266b20b313364a74b16c9ac45d089b1e9
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/11/2019
ms.locfileid: "54220142"
---
# <a name="containers-modern-c"></a>컨테이너(모던 C++)

기본적으로 C++에서 기본 순차 컨테이너로서의 [vector](../standard-library/vector-class.md)를 사용합니다. 이것은 .NET 언어에서의 `List<T>`와 동일합니다.

```cpp
vector<string> apples;
apples.push_back("Granny Smith");
```

기본 연관 컨테이너로 [map](../standard-library/map-class.md)(`unordered_map`이 아님)을 사용합니다. 디제너레이트 및 다중 사례에 대해 [set](../standard-library/set-class.md), [multimap](../standard-library/multimap-class.md), [multiset](../standard-library/multiset-class.md)을 사용합니다.

```cpp
map<string, string> apple_color;
// ...
apple_color["Granny Smith"] = "Green";
```

성능 최적화가 필요하면 다음을 사용합니다.

- 합니다 [배열](../standard-library/array-class-stl.md) 포함 하는 것이 중요 클래스 멤버로 예를 들어을 입력 합니다.

- 연관 컨테이너와 같은 순서가 지정 되지 않은 [unordered_map](../standard-library/unordered-map-class.md)합니다. 이러한 요소 마다 낮은 오버 헤드 있고 일정 시간 조회 되지만 있을 수 있습니다 정확 하 고 효율적으로 사용 하기 어렵습니다.

- 정렬된 `vector`. 더 자세한 내용은 [Algorithms](../cpp/algorithms-modern-cpp.md)을 참조하세요.

C 스타일 배열을 사용 하지 마세요. 직접 데이터에 대 한 액세스가 필요한 이전 api를 사용 하 여 접근자 메서드 같은 `f(vec.data(), vec.size());` 대신 합니다.

컨테이너에 대한 다른 문서를 보려면 [C++ 표준 라이브러리 컨테이너](../standard-library/stl-containers.md)를 참조하십시오.

## <a name="see-also"></a>참고 항목

[C++의 진화(모던 C++)](../cpp/welcome-back-to-cpp-modern-cpp.md)<br/>
[C++ 언어 참조](../cpp/cpp-language-reference.md)<br/>
[C++ 표준 라이브러리](../standard-library/cpp-standard-library-reference.md)
