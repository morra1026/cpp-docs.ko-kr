---
title: 컴파일러 오류 C2603
ms.date: 11/04/2016
f1_keywords:
- C2603
helpviewer_keywords:
- C2603
ms.assetid: 9ca520d0-f082-4b65-933d-17c3bcf8b02c
ms.openlocfilehash: 5391aed09b7fd448a9d72ea7cc17cd5c26fc5f04
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50605766"
---
# <a name="compiler-error-c2603"></a>컴파일러 오류 C2603

> '*함수*': 생성자/소멸자 함수에서 사용 하 여 너무 많은 블록 범위 정적 개체

버전의 Visual Studio 2015 이전 Visual c + + 컴파일러에서 때나 합니다 [/zc: threadsafeinit-](../../build/reference/zc-threadsafeinit-thread-safe-local-static-initialization.md) 컴파일러 옵션을 지정 하면 31 외부에 표시 되는 인라인 함수에서 사용할 수 있습니다 하는 정적 개체의 수에 제한이 있기 .

이 문제를 해결 하려면 최신 버전의 Visual c + + 컴파일러 도구 집합을 채택 하거나 가능한 경우 /zc: threadsafeinit-컴파일러 옵션을 제거는 것이 좋습니다. 없는 경우에 정적 개체를 결합 하는 것이 좋습니다. 개체가 동일한 형식의 경우 해당 유형의 단일 정적 배열 사용 하는 것이 좋습니다를 필요에 따라 개별 멤버를 참조 합니다.

## <a name="example"></a>예제

다음 코드는 C2603를 생성 하 고를 해결 하는 방법을 보여 줍니다.

```cpp
// C2603.cpp
// Compile by using: cl /W4 /c /Zc:threadSafeInit- C2603.cpp
struct C { C() {} };
extern inline void f1() {
    static C C01, C02, C03, C04, C05, C06, C07, C08, C09, C10;
    static C C11, C12, C13, C14, C15, C16, C17, C18, C19, C20;
    static C C21, C22, C23, C24, C25, C26, C27, C28, C29, C30, C31;
    static C C32;   // C2603 Comment this line out to avoid error
}
```
