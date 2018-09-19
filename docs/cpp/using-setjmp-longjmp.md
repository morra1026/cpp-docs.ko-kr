---
title: Setjmp 및 longjmp 사용 | Microsoft Docs
ms.custom: ''
ms.date: 08/14/2018
ms.technology:
- cpp-language
ms.topic: language-reference
f1_keywords:
- longjmp_cpp
- setjmp_cpp
dev_langs:
- C++
helpviewer_keywords:
- C++ exception handling, setjmp/longjmp functions
- setjmpex.h
- longjmp function in C++ programs
- setjmp.h
- setjmp function
- setjmp function, C++ programs
ms.assetid: 96be8816-f6f4-4567-9a9c-0c3c720e37c5
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 711d829ea3393041c713fbb042318b680100a52a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46111955"
---
# <a name="using-setjmp-and-longjmp"></a>Setjmp 및 longjmp 사용

때 [setjmp](../c-runtime-library/reference/setjmp.md) 하 고 [longjmp](../c-runtime-library/reference/longjmp.md) 는 로컬이 아닌를 실행 하는 방법을 제공 함께 사용 하는 **goto**합니다. 이러한 표준 호출을 사용 하지 않고 전에 호출된 된 루틴에서 오류 처리 또는 복구 코드에 실행 제어를 전달할 C 코드에서 일반적으로 사용 되 나 반환 규칙.

> [!CAUTION]
> 때문에 `setjmp` 고 `longjmp` 를 지원 하지 않고 올바른 c + + 컴파일러 간에 이식 스택 프레임 개체 소멸 지역 변수의 최적화를 막아 성능을 저하 시킬 수 있으므로, c + +에서 사용 되는 권장 되지 않습니다 프로그램입니다. 사용 하는 것이 좋습니다 **시도** 하 고 **catch** 대신 생성 합니다.

사용 하려는 경우 `setjmp` 하 고 `longjmp` c + + 프로그램에서 포함 \<setjmp.h > 또는 \<setjmpex.h > 함수와 구조적 예외 처리 (SEH) 또는 c + + 예외 간에 올바른 상호 작용이 수행 하기 위해 처리 합니다.

**Microsoft 전용**

사용 하는 경우는 [/EH](../build/reference/eh-exception-handling-model.md) 옵션을 c + + 코드, 스택 해제 중 로컬 개체에 대 한 소멸자가 호출 됩니다. 그러나 사용 하는 경우 **/EHs** 하거나 **/EHsc** 컴파일 및 사용 하는 함수 중 하나를 [noexcept](../cpp/noexcept-cpp.md) 호출 `longjmp`, 해당 함수에 대 한 소멸자를 해제 한 다음 최적화 프로그램 상태에 따라, 발생할 수 있습니다.

이식 가능한 코드의 경우는 `longjmp` 호출이 실제로 실행을 잘못 프레임 기반 개체가 소멸은 명시적으로 반드시 표준 및 다른 컴파일러에서 지원 되지 않습니다. 경고 수준 4에서 호출을 알 수 있도록 `setjmp` C4611 경고 발생: 'j 및 c + + 개체 소멸 사이의 상호 작용이 이식 가능 하지 않습니다.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고자료

[C(구조적) 및 C++ 예외 혼합](../cpp/mixing-c-structured-and-cpp-exceptions.md)
