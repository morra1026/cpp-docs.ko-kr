---
title: /Gh(_penter 후크 함수 사용)
ms.date: 11/04/2016
f1_keywords:
- _penter
helpviewer_keywords:
- /Gh compiler option [C++]
- Gh compiler option [C++]
- _penter function
- -Gh compiler option [C++]
ms.assetid: 1510a082-8a0e-486e-a309-6add814b494f
ms.openlocfilehash: bf7734a7b81c9550c060d43c2eabf5cb05332407
ms.sourcegitcommit: 8105b7003b89b73b4359644ff4281e1595352dda
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57820535"
---
# <a name="gh-enable-penter-hook-function"></a>/Gh(_penter 후크 함수 사용)

에 대 한 호출으로 인해는 `_penter` 모든 메서드 또는 함수의 시작 함수입니다.

## <a name="syntax"></a>구문

```
/Gh
```

## <a name="remarks"></a>설명

합니다 `_penter` 함수 라이브러리의 일부가 아니며에 대 한 정의 제공 하는 것 `_penter`입니다.

명시적으로 호출 하려는 경우가 아니면 `_penter`, 프로토타입을 제공 해야 합니다. 함수 처럼 다음과 같은 프로토타입의 되었 및 항목에 대해 모든 레지스터의 콘텐츠를 푸시 하며 종료 시 변경 되지 않은 콘텐츠를 pop에 나타나야 합니다.

```
void __declspec(naked) __cdecl _penter( void );
```

이 선언은 64 비트 프로젝트에 대 한 제공 되지 않습니다.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 컴파일러 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 참조 하세요 [Visual Studio에서 설정 c + + 컴파일러 및 빌드 속성](../working-with-project-properties.md)합니다.

1. **C/C++** 폴더를 클릭합니다.

1. **명령줄** 속성 페이지를 클릭합니다.

1. **추가 옵션** 상자에 컴파일러 옵션을 입력합니다.

### <a name="to-set-this-compiler-option-programmatically"></a>프로그래밍 방식으로 이 컴파일러 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions%2A>을 참조하세요.

## <a name="example"></a>예제

다음 코드를 사용 하 여 컴파일하면 **/Gh**를 보여 줍니다 어떻게 `_penter` 두 번 호출 됩니다 함수를 입력할 때 한 번 `main` 함수를 입력할 때 한 번 `x`합니다.

```cpp
// Gh_compiler_option.cpp
// compile with: /Gh
// processor: x86
#include <stdio.h>
void x() {}

int main() {
   x();
}

extern "C" void __declspec(naked) __cdecl _penter( void ) {
   _asm {
      push eax
      push ebx
      push ecx
      push edx
      push ebp
      push edi
      push esi
    }

   printf_s("\nIn a function!");

   _asm {
      pop esi
      pop edi
      pop ebp
      pop edx
      pop ecx
      pop ebx
      pop eax
      ret
    }
}
```

```Output
In a function!
In a function!
```

## <a name="see-also"></a>참고자료

[MSVC 컴파일러 옵션](compiler-options.md)<br/>
[MSVC 컴파일러 명령줄 구문](compiler-command-line-syntax.md)
