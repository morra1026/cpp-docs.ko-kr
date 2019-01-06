---
title: C++ 예외 처리
ms.date: 11/04/2016
helpviewer_keywords:
- C++ exception handling
- Visual C++, exception handling
ms.assetid: 65f80b44-9d0f-4d17-b910-07205a5c5c40
ms.openlocfilehash: b4eaab7d5bb352cccc612dd950572464b82b67e8
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50614749"
---
# <a name="c-exception-handling"></a>C++ 예외 처리

C++ 언어에는 예외의 throw 및 catch를 기본적으로 지원합니다. C++에서 프로그래밍하는 경우 이 단원에서 설명한 대로 기본 제공 C++ 예외 지원을 거의 항상 사용해야 합니다.

코드에서 C++ 예외 처리를 사용하려면 [/EHsc](../build/reference/eh-exception-handling-model.md)를 사용합니다.

## <a name="in-this-section"></a>단원 내용

C++ 예외 처리에 대한 이 설명에는 다음이 포함됩니다.

- [Try, catch 및 throw 문](../cpp/try-throw-and-catch-statements-cpp.md)

- [Catch 블록의 평가 방법](../cpp/how-catch-blocks-are-evaluated-cpp.md)

- [예외 및 스택 해제](../cpp/exceptions-and-stack-unwinding-in-cpp.md)

- [예외 사양](../cpp/exception-specifications-throw-cpp.md)

- [noexcept](../cpp/noexcept-cpp.md)

- [처리되지 않은 C++ 예외](../cpp/unhandled-cpp-exceptions.md)

- [C(구조적) 및 C++ 예외 혼합](../cpp/mixing-c-structured-and-cpp-exceptions.md)

## <a name="support-for-earlier-mfc-exceptions"></a>이전 MFC 예외 지원

버전 4.0부터 MFC는 C++ 예외 처리 메커니즘을 사용합니다. 새 코드에서는 C++ 예외 처리를 사용하는 것이 좋지만 MFC 버전 4.0 이상은 기존 코드의 연결이 끊어지지 않도록 MFC의 이전 버전의 매크로를 유지합니다. 매크로 및 새 메커니즘도 결합할 수 있습니다. 매크로와 C++ 예외 처리 혼합 및 기존 코드를 변환하여 새로운 메커니즘을 사용하는 방법에 대한 자세한 내용은 [예외: MFC 매크로 및 C++ 예외 사용](../mfc/exceptions-using-mfc-macros-and-cpp-exceptions.md) 및 [예외: MFC 예외 매크로에서 변환](../mfc/exceptions-converting-from-mfc-exception-macros.md) 문서를 참조하세요. 이전 MFC 예외 매크로를 계속 사용하는 경우 C++ 예외 키워드로 평가합니다. [예외: 버전 3.0의에서 예외 매크로 변경 사항](../mfc/exceptions-changes-to-exception-macros-in-version-3-0.md)을 참조하세요.

## <a name="see-also"></a>참고 항목

[예외 처리](../cpp/exception-handling-in-visual-cpp.md)
