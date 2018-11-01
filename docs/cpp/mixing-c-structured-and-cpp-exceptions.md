---
title: C (구조적) 및 c + + 예외 혼합
ms.date: 08/14/2018
helpviewer_keywords:
- exceptions [C++], mixed C and C++
- C++ exception handling, mixed-language
- structured exception handling [C++], mixed C and C++
- catch keyword [C++], mixed
- try-catch keyword [C++], mixed-language
ms.assetid: a149154e-36dd-4d1a-980b-efde2a563a56
ms.openlocfilehash: 94d6dc249cb130aaf09d3202b9e8f437d00a9597
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50548205"
---
# <a name="mixing-c-structured-and-c-exceptions"></a>C (구조적) 및 c + + 예외 혼합

이식 가능한 코드를 작성 하려는 경우의 구조적된 예외 처리 (SEH)는 c + + 프로그램의 사용이 권장 되지 않습니다. 그러나 사용 하 여 컴파일하고 하려는 경우도 [/EHa](../build/reference/eh-exception-handling-model.md) 구조적된 예외와 c + + 소스 코드를 조합 하 고 두 종류의 예외를 처리 하기 위한 일부 기능이 필요 합니다. 구조적된 예외 처리기 개체 또는 형식화 된 예외의 개념이 있으므로 c + + 코드에서 throw 된 예외를 처리할 수 없습니다. 그러나 c + + **catch** 처리기는 구조화 된 예외를 처리할 수 있습니다. C + + 예외 처리 구문을 (**시도**, **throw**하십시오 **catch**)는 C 컴파일러의 경우 구조적된 예외 처리 구문을에서 허용 되지 않습니다 (**__try**하십시오 **__except**, **__finally**) c + + 컴파일러에서 지원 됩니다.

참조 [_set_se_translator](../c-runtime-library/reference/set-se-translator.md) 구조화 된 예외를 c + + 예외로 처리 하는 방법에 대 한 정보에 대 한 합니다.

구조화 된 혼합 하면 및 c + + 예외를 이러한 잠재적인 문제에 유의 합니다.

- C++ 예외 및 구조화된 예외는 동일한 함수 내에서 혼합될 수 없습니다.

- 종료 처리기 (**__finally** 블록) 예외가 throw 된 후 해제 하는 동안에 항상 실행 됩니다.

- C + + 예외 처리를 catch 할 수 및 preserve로 컴파일된 모든 모듈의 의미 체계를 해제 합니다 [/EH](../build/reference/eh-exception-handling-model.md) 컴파일러 옵션을 해제 의미 체계는 사용 합니다.

- 소멸자 함수가 모든 개체에 대해 호출하지 않는 일부 경우가 있을 수 있습니다. 예를 들어, 함수는 초기화 되지 않은 함수 포인터를 통해 호출 하는 동안 구조화 된 예외를 발생 하는 경우 해당 함수 호출 전에 생성 된 매개 변수 개체는 해당 개체의 소멸자가 호출 되지 않습니다. 중 스택 해제 합니다.

## <a name="next-steps"></a>다음 단계

- [C + + 프로그램에서 setjmp 또는 longjmp 사용](../cpp/using-setjmp-longjmp.md)

  사용에 대 한 자세한 내용은 `setjmp` 고 `longjmp` c + + 프로그램에서입니다.

- [C++에서 구조적 예외 처리](../cpp/exception-handling-differences.md)

  C + +를 사용 하 여 예외 처리를 구성 하는 방법의 예제를 참조 하세요.

## <a name="see-also"></a>참고자료

[C++ 예외 처리](../cpp/cpp-exception-handling.md)
