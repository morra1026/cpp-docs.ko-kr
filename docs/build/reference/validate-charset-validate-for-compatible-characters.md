---
title: /validate-charset (호환 문자에 대 한 유효성 검사)
ms.date: 11/04/2016
f1_keywords:
- /validate-charset
- validate-charset
helpviewer_keywords:
- /validate-charset compiler option
ms.assetid: 50360fd0-4d32-4a4f-95d0-53d38c12ad4c
ms.openlocfilehash: 243d225f5acde0c6099050539687726ea082c898
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50590491"
---
# <a name="validate-charset-validate-for-compatible-characters"></a>/validate-charset (호환 문자에 대 한 유효성 검사)

소스 파일 텍스트를 표현할 수 있는 문자만 포함 되어 있는지 확인 u t F-8로 합니다.

## <a name="syntax"></a>구문

```
/validate-charset[-]
```

## <a name="remarks"></a>설명

사용할 수는 **/validate-charset** 소스 문자 나타낼 수 있는 문자 집합과 실행 문자 집합에 소스 코드를 포함 하는 유효성을 검사 하는 옵션입니다. 지정 하는 경우이 확인을 자동으로 사용 **/source-charset**하십시오 **/execution-charset**, 또는 **/utf-8** 컴파일러 옵션입니다. 지정 하 여이 검사를 명시적으로 비활성화할 수 있습니다는 **유효성 검사 /-문자 집합-** 옵션입니다.

Visual Studio는 기본적으로 인지 하는 경우 소스 파일 인코딩된 유니코드 형식으로 예를 들어, utf-16 또는 u t F-8 바이트 순서 표시를 검색 합니다. 바이트 순서 표시가 없는 경우 소스 파일은 인코딩된 현재 사용자 코드 페이지를 사용 하는 코드 페이지를 사용 하 여 지정 하지 않으면 가정 **/utf-8** 또는 **/source-charset** 옵션입니다. Visual Studio를 사용 하면 여러 문자 인코딩 중 하나를 사용 하 여 c + + 소스 코드를 저장할 수 있습니다. 소스 및 실행 문자 집합에 대 한 정보를 참조 하세요 [문자 집합](../../cpp/character-sets.md) 언어 설명서에 있습니다. 문자 집합 이름 목록이 지원 코드 페이지 식별자를 참조 하세요 [코드 페이지 식별자](/windows/desktop/Intl/code-page-identifiers)합니다.

Visual Studio는 소스 문자 집합과 실행 문자 집합 변환 시 내부 문자 인코딩 u t F-8을 사용 합니다. 실행 문자 집합의 원본 파일의 문자를 나타낼 수 없으면, u t F-8 변환 물음표를 대체 하는 '?' 문자입니다. 합니다 **/validate-charset** 옵션을 사용 하면이 문제가 발생 하면 경고를 보고 하려면 컴파일.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 컴파일러 옵션을 설정하려면

1. 프로젝트 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. 확장 된 **구성 속성**, **C/c + +** 를 **명령줄** 폴더입니다.

1. **고급 옵션**를 추가 합니다 **/validate-charset** 옵션을 선택한 기본 인코딩을 지정 합니다.

1. 선택할 **확인** 변경 내용을 저장 합니다.

## <a name="see-also"></a>참고 항목

[컴파일러 옵션](../../build/reference/compiler-options.md)<br/>
[컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md)<br/>
[/execution-charset (실행 문자 집합 설정)](../../build/reference/execution-charset-set-execution-character-set.md)<br/>
[/source-charset(소스 문자 집합 설정)](../../build/reference/source-charset-set-source-character-set.md)<br/>
[/utf-8(소스 및 실행 파일 문자 집합을 UTF-8로 설정)](../../build/reference/utf-8-set-source-and-executable-character-sets-to-utf-8.md)