---
title: /Za, /Ze(언어 확장명 사용 안 함)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCCLWCECompilerTool.DisableLanguageExtensions
- /za
- /ze
- VC.Project.VCCLCompilerTool.DisableLanguageExtensions
helpviewer_keywords:
- -Za compiler option [C++]
- Za compiler option [C++]
- language extensions, disabling in compiler
- -Ze compiler option [C++]
- language extensions
- enable language extensions
- /Za compiler option [C++]
- /Ze compiler option [C++]
- Disable Language Extensions compiler option
- Ze compiler option [C++]
ms.assetid: 65e49258-7161-4289-a176-7c5c0656b1a2
ms.openlocfilehash: a3d25f71739f9948f2c0237efbaeaf8fa89f2114
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50549723"
---
# <a name="za-ze-disable-language-extensions"></a>/Za, /Ze(언어 확장명 사용 안 함)

합니다 **/Za** 컴파일러 옵션은 ANSI C89 또는 C + + 11 ISO와 호환 되지 않는 언어 구문에 대 한 오류를 생성 합니다. 합니다 **/Ze** 기본적으로 켜져 컴파일러 옵션에 대 한 Microsoft 확장 사용 하도록 설정 합니다.

## <a name="syntax"></a>구문

```
/Za
/Ze
```

## <a name="remarks"></a>설명

> [!NOTE]
>  합니다 **/Ze** 동작 기본적으로 켜져 있으므로 옵션은 사용 되지 않습니다. 사용 하는 것이 좋습니다 합니다 [/Zc (규칙)](../../build/reference/zc-conformance.md) 컴파일러 옵션을 특정 언어 확장 기능을 제어 합니다. 사용 되지 않는 컴파일러 옵션의 목록을 참조 하세요. 합니다 **컴파일러 옵션 및 사용 되지 않음** 섹션 [컴파일러 옵션 범주별 목록](../../build/reference/compiler-options-listed-by-category.md)합니다.

Visual c + + 컴파일러는 다양 한 ANSI C89, ISO C99 또는 ISO c + + 표준에 지정 된 수준을 넘어선 기능을 제공합니다. 이러한 기능은 C 및 c + +에 대 한 Microsoft 확장으로 전체적으로 알려져 있습니다. 이러한 확장은 기본적으로 사용 가능 하 고 사용할 수 없는 경우는 **/Za** 옵션을 지정 합니다. 특정 확장에 대 한 자세한 내용은 참조 하세요. [C 및 c + +에 대 한 Microsoft 확장](../../build/reference/microsoft-extensions-to-c-and-cpp.md)합니다.

언어 확장을 사용 하지 않도록 지정 하 여는 것이 좋습니다 합니다 **/Za** 프로그램의 다른 환경으로 이식 하려는 경우 옵션입니다. 때 **/Za** 를 지정 하면 컴파일러는 Microsoft 확장으로 단순 식별자는 키워드를 처리, 다른 Microsoft 확장을 사용 하지 않도록 설정 하 고 자동으로 정의 된 `__STDC__` C 프로그램에 대 한 미리 정의 된 매크로입니다.

다른 컴파일러 옵션을 사용 하 여 사용 **/Za** 컴파일러에서 표준 규칙을 준수 하는 방법에 영향을 줄 수 있습니다.

특정 표준을 준수 하는 동작 설정을 지정 하는 방법에 대해서는 [/Zc](../../build/reference/zc-conformance.md) 컴파일러 옵션입니다.

Visual c + +를 사용 하 여 규칙과 관련 된 문제에 대 한 자세한 내용은 참조 하세요. [비표준 동작](../../cpp/nonstandard-behavior.md)합니다.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 컴파일러 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. 탐색 창에서 선택 **구성 속성**, **C/c + +** 하십시오 **언어**합니다.

1. 수정 된 **언어 확장 사용 안 함** 속성입니다.

### <a name="to-set-this-compiler-option-programmatically"></a>프로그래밍 방식으로 이 컴파일러 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.DisableLanguageExtensions%2A>을 참조하세요.

## <a name="see-also"></a>참고 항목

[컴파일러 옵션](../../build/reference/compiler-options.md)<br/>
[컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md)<br/>
[/Zc(규칙)](../../build/reference/zc-conformance.md)
