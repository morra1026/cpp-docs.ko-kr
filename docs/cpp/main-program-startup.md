---
title: 'main: 프로그램 시작'
ms.date: 11/04/2016
f1_keywords:
- vc.main.startup
- _tmain
helpviewer_keywords:
- program startup [C++]
- entry points, program
- wmain function
- _tmain function
- startup code, main function
- main function, program startup
ms.assetid: f9581cd6-93f7-4bcd-99ec-d07c3c107dd4
ms.openlocfilehash: 76c580d4b48e1651803ae9bf62f0e2346e19e06c
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50603283"
---
# <a name="main-program-startup"></a>main: 프로그램 시작

특수함수인 **main**은 모든 C와 C++ 프로그램의 실행 시작 지점입니다. 유니코드 프로그래밍 모델을 준수하는 코드를 작성하는 경우 와이드 문자 기반의 **main**함수인 `wmain`을 사용할 수 있습니다.

합니다 **주** 함수는 컴파일러에서 미리 정의 되지 않습니다. 프로그램 텍스트에서 제공되어야 합니다.
**main** 함수는 컴파일러에 미리 정의되어 있지 않습니다. 프로그램 소스코드 상에서 제공해야합니다.

**main**에 대한 선언은 다음과 같습니다.

```cpp
int main();
```

또는 필요에 따라 다음과 같은 선언 구문을 사용할 수 있습니다.

```cpp
int main(int argc, char *argv[], char *envp[]);
```

## <a name="microsoft-specific"></a>Microsoft 전용

`wmain`의 선언 구문은 다음과 같습니다.

```cpp
int wmain( );
```

또는 필요에 따라 다음과 같은 선언 구문을 사용할 수 있습니다.

```cpp
int wmain(int argc, wchar_t *argv[], wchar_t *envp[]);
```

tchar.h에 정의된 `_tmain`을 사용할 수도 있습니다. _UNICODE가 정의되어 있다면 `_tmain`은 `wmain`으로 정의됩니다. 그렇지 않다면 `_tmain`은 **main**으로 확인됩니다.

**main** 및 `wmain` 함수를 **void**(반환 값 없음)형식을 반환하는 것으로 선언 할 수도 있습니다. **main** 이나 `wmain`이 **void** 형식을 반환한다고 선언하면 [return](../cpp/return-statement-in-program-termination-cpp.md)문을 사용하여 부모 프로세스나 운영 체제에 종료코드를 반환 할 수 없습니다. **main** 또는 `wmain`의 반환 형식을 **void**로 선언했을 때 종료코드를 반환하려면 [exit](../cpp/exit-function.md) 함수를 사용해야 합니다.

**Microsoft 전용 종료**

`argc` 및 `argv`의 형식은 언어에 의해 정의됩니다. `argc`, `argv` 및 `envp`라는 이름은 일반적으로 사용되지만 컴파일러는 필요하지 않습니다. 자세한 내용 및 예제는 [인수 정의](../cpp/argument-definitions.md)를 참조합니다.

## <a name="see-also"></a>참고자료

[키워드](../cpp/keywords-cpp.md)<br/>
[main 대신 wmain 사용](../cpp/using-wmain-instead-of-main.md)<br/>
[main 함수 제한](../cpp/main-function-restrictions.md)<br/>
[C++ 명령줄 인수 구문 분석](../cpp/parsing-cpp-command-line-arguments.md)
