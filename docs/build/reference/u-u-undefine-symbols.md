---
title: -U, u (기호 정의 해제) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- VC.Project.VCCLCompilerTool.UndefinePreprocessorDefinitions
- VC.Project.VCCLWCECompilerTool.UndefinePreprocessorDefinitions
- VC.Project.VCCLCompilerTool.UndefineAllPreprocessorDefinitions
- /u
- VC.Project.VCCLWCECompilerTool.UndefineAllPreprocessorDefinitions
dev_langs:
- C++
helpviewer_keywords:
- -U compiler option [C++]
- Undefine Symbols compiler option
- /U compiler option [C++]
- U compiler option [C++]
ms.assetid: 7bc0474f-6d1f-419b-807d-0d8816763b2a
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 34030a8ef91e5a25bdb1a13981925c5ddf1f05df
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45721554"
---
# <a name="u-u-undefine-symbols"></a>/U, /u(기호 정의 해제)

합니다 **/U** 컴파일러 옵션에 지정된 된 전처리기 기호 정의 해제 합니다. 합니다 **/u** 컴파일러 옵션에는 컴파일러가 정의 하는 Microsoft 전용 기호 정의 해제 합니다.

## <a name="syntax"></a>구문

```
/U[ ]symbol
/u
```

## <a name="arguments"></a>인수

*기호*<br/>
전처리기 기호 정의 해제입니다.

## <a name="remarks"></a>설명

모두를 **/U** 또는 **/u** 옵션 사용 하 여 만든 기호의 정의 해제할 수 있습니다는 **#define** 지시문입니다.

**/U** 옵션 사용 하 여 이전에 정의 된 기호의 정의 해제할 수는 **/D** 옵션.

기본적으로 컴파일러는 다음과 같은 Microsoft 관련 기호를 정의합니다.

|기호|기능|
|------------|--------------|
|_CHAR_UNSIGNED|기본 char 형식은 부호가 없습니다. 경우 정의 된 [/J](../../build/reference/j-default-char-type-is-unsigned.md) 옵션을 지정 합니다.|
|_CPPRTTI|로 컴파일된 코드에 대해 정의 된 [/GR](../../build/reference/gr-enable-run-time-type-information.md) 옵션입니다.|
|_CPPUNWIND|로 컴파일된 코드에 대해 정의 된 [/EHsc](../../build/reference/eh-exception-handling-model.md) 옵션입니다.|
|_DLL|경우 정의 된 [/MD](../../build/reference/md-mt-ld-use-run-time-library.md) 옵션을 지정 합니다.|
|_M_IX86|기본적으로 x86에 대해 600으로 정의 된 대상입니다.|
|_MSC_VER|자세한 내용은 [Predefined Macros](../../preprocessor/predefined-macros.md)을 참조하십시오.|
|_WIN32|WIN32 응용 프로그램에 대 한 정의. 항상 정의되어 있습니다.|
|_MT|경우 정의 된 [/MD 또는 /MT](../../build/reference/md-mt-ld-use-run-time-library.md) 옵션을 지정 합니다.|

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 컴파일러 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. **C/C++** 폴더를 클릭합니다.

1. 클릭 합니다 **고급** 속성 페이지.

1. 수정 된 **전처리기 정의 해제** 하거나 **모든 전처리기 정의 해제** 속성입니다.

### <a name="to-set-this-compiler-option-programmatically"></a>프로그래밍 방식으로 이 컴파일러 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.UndefineAllPreprocessorDefinitions%2A> 또는 <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.UndefinePreprocessorDefinitions%2A>을 참조하십시오.

## <a name="see-also"></a>참고 항목

[컴파일러 옵션](../../build/reference/compiler-options.md)<br/>
[컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md)<br/>
[/J (부호 형식은 기본 문자)](../../build/reference/j-default-char-type-is-unsigned.md)
[/GR (런타임 형식 정보 사용)](../../build/reference/gr-enable-run-time-type-information.md)
[/EH (예외 처리 모델)](../../build/reference/eh-exception-handling-model.md) 
 [/MD, /MT, /LD (런타임 라이브러리 사용)](../../build/reference/md-mt-ld-use-run-time-library.md)