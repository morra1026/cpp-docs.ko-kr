---
title: /F(스택 크기 설정)
ms.date: 11/04/2016
f1_keywords:
- /f
helpviewer_keywords:
- set stack size compiler option
- F compiler option [C++]
- -F compiler option [C++]
- /F compiler option [C++]
- stack, setting size
ms.assetid: 17320b6f-8305-445b-9ec2-75833f4b29e0
ms.openlocfilehash: 69d26a4e4634ea60457d75bc97d2266036d11e10
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50525530"
---
# <a name="f-set-stack-size"></a>/F(스택 크기 설정)

프로그램의 스택 크기를 바이트 단위로 설정 합니다.

## <a name="syntax"></a>구문

> **/F** *수*

## <a name="arguments"></a>인수

*수*<br/>
스택 크기 (바이트)입니다.

## <a name="remarks"></a>설명

이 옵션이 없으면 스택 크기를 1MB로 기본값은입니다. 합니다 *번호* 인수 10 진수 또는 C 언어 표기법에 있을 수 있습니다. 인수는 1에서 링커에 의해 허용 된 최대 스택 크기까지 수 있습니다. 링커는 가장 가까운 4 바이트에 지정된 된 값으로 반올림합니다. 사이 공백을 **/F** 하 고 *수* 선택 사항입니다.

프로그램 스택 오버플로 메시지를 가져오는 경우 스택 크기를 증가 해야 합니다.

또한 스택 크기를 설정할 수 있습니다.

- 사용 하 여 **스택/** 링커 옵션입니다. 자세한 내용은 [스택/](../../build/reference/stack.md)합니다.

- .Exe 파일에서 EDITBIN를 사용합니다. 자세한 내용은 [EDITBIN 참조](../../build/reference/editbin-reference.md)합니다.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 컴파일러 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. 선택 된 **구성 속성** > **C/c + +** > **명령줄** 속성 페이지.

1. **추가 옵션** 상자에 컴파일러 옵션을 입력합니다.

### <a name="to-set-this-compiler-option-programmatically"></a>프로그래밍 방식으로 이 컴파일러 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions%2A>을 참조하세요.

## <a name="see-also"></a>참고 항목

[컴파일러 옵션](../../build/reference/compiler-options.md)<br/>
[컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md)