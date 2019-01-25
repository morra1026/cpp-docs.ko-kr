---
title: '주: 프로그램 시작'
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
ms.openlocfilehash: 358ae8ec88281bab741393b1196ee2a1e615e896
ms.sourcegitcommit: c85c8a1226d8fbbaa29f4691ed719f8e6cc6575c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54894304"
---
# <a name="main-program-startup"></a>주: 프로그램 시작

이라는 특수 함수 **주** 모든 C 및 c + + 프로그램에 대 한 실행의 시작 지점입니다. 유니코드 프로그래밍 모델을 따르는 코드를 작성 하는, 하는 경우 사용할 수 있습니다 `wmain`의 와이드 문자 버전인 **주**합니다.

합니다 **주** 함수는 컴파일러에서 미리 정의 되지 않습니다. 프로그램 텍스트에서 제공되어야 합니다.

선언 구문은 **주** 는

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

사용할 수도 있습니다 `_tmain`, tchar.h에서 정의 됩니다. `_tmain` 로 확인 되 **주** _UNICODE가 정의 합니다. _UNICODE가 정의된 경우에는 `_tmain`이 `wmain`으로 확인됩니다.

또는 합니다 **주** 하 고 `wmain` 반환 하도록 함수를 선언할 수 있습니다 **void** (반환 값 없음). 선언 하는 경우 **주** 또는 `wmain` 반환 **void**를 사용 하 여 부모 프로세스나 운영 체제 종료 코드를 반환할 수 없습니다는 [반환](../cpp/return-statement-in-program-termination-cpp.md) 문입니다. 경우는 종료 코드를 반환할 **주** 또는 `wmain` 로 선언 됩니다 **void**를 사용 해야 합니다는 [종료](../cpp/exit-function.md) 함수입니다.

**Microsoft 전용 종료**

`argc` 및 `argv`의 형식은 언어에서 정의됩니다. `argc`, `argv` 및 `envp`라는 이름이 일반적으로 사용되지만 컴파일러에서 필요하지는 않습니다. 자세한 내용 및 예제를 참조 하세요 [인수 정의](../cpp/argument-definitions.md)합니다.

## <a name="see-also"></a>참고자료

[키워드](../cpp/keywords-cpp.md)<br/>
[main 대신 wmain 사용](../cpp/using-wmain-instead-of-main.md)<br/>
[main 함수 제한](../cpp/main-function-restrictions.md)<br/>
[C++ 명령줄 인수 구문 분석](../cpp/parsing-cpp-command-line-arguments.md)
