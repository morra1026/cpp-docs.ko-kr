---
title: main 함수 제한
ms.date: 11/04/2016
f1_keywords:
- Main
helpviewer_keywords:
- main function, restrictions on using
ms.assetid: 7b3df731-344b-44a8-850c-11cbcbfbfa83
ms.openlocfilehash: 9ccea987b05c7854e78ba1621fd6c0a065d73d5a
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50555740"
---
# <a name="main-function-restrictions"></a>main 함수 제한

다른 모든 C++ 함수에는 적용되지 않는 **`main`** 함수에 대한 제한이 몇 가지 있습니다. **`main`** 함수에 대한 제한은 다음과 같습니다.

- 오버로드될 수 없습니다([오버로드](function-overloading.md) 참조).

- **`inline`** 으로 선언될 수 없습니다.

- **`static`** 으로 선언될 수 없습니다.

- 주소를 사용할 수 없습니다.

- 호출할 수 없습니다.

## <a name="see-also"></a>참고

[main: 프로그램 시작](../cpp/main-program-startup.md)