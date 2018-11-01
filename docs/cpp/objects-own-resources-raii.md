---
title: 개체가 리소스 소유(RAII)
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: f86b484e-5a27-4c3b-a92a-dfaa5dd6d93a
ms.openlocfilehash: a10d6c2177c391ead6065767994b09fb6236ee3a
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50593612"
---
# <a name="objects-own-resources-raii"></a>개체가 리소스 소유(RAII)

고유한 리소스 개체는 있는지 확인 합니다. 이 원칙은 라고도 하며 "resource acquisition is 초기화" 또는 "RAII."

## <a name="example"></a>예제

생성자 인수로 (거의 항상 unique_ptr) 소유 하는 다른 명명 된 개체에 "새" 모든 개체를 전달 합니다.

```cpp
void f() {
    unique_ptr<widget> p( new widget() );
    my_class x( new widget() );
    // ...
} // automatic destruction and deallocation for both widget objects
  // automatic exception safety, as if "finally { p->dispose(); x.w.dispose(); }"
```

소유 하는 다른 개체에 새 리소스를 항상 즉시 전달 합니다.

```cpp
void g() {
    other_class y( OpenFile() );
    // ...
} // automatic closing and release for file resource
  // automatic exception safety, as if "finally { y.file.dispose(); }"
```

## <a name="see-also"></a>참고자료

[C++의 진화](../cpp/welcome-back-to-cpp-modern-cpp.md)<br/>
[C++ 언어 참조](../cpp/cpp-language-reference.md)<br/>
[C++ 표준 라이브러리](../standard-library/cpp-standard-library-reference.md)