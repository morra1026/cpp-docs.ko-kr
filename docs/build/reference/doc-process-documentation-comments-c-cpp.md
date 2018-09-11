---
title: -doc (문서 주석 처리) (C/c + +) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- VC.Project.VCCLCompilerTool.GenerateXMLDocumentationFiles
- /doc
- VC.Project.VCCLCompilerTool.XMLDocumentationFileName
dev_langs:
- C++
helpviewer_keywords:
- /doc compiler option [C++]
- comments, C++ code
- XML documentation, comments in source files
- -doc compiler option [C++]
ms.assetid: b54f7e2c-f28f-4f46-9ed6-0db09be2cc63
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ee09b3fe61c86015d8dc7464ef9925419fc745d9
ms.sourcegitcommit: 761c5f7c506915f5a62ef3847714f43e9b815352
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44100342"
---
# <a name="doc-process-documentation-comments-cc"></a>/doc(문서 주석 처리)(C/C++)
컴파일러에서 문서 주석을 처리 소스 코드 파일에 문서 주석이 포함 된 각 소스 코드 파일에 대 한.xdc 파일을 만듭니다.

## <a name="syntax"></a>구문

> **/doc**[*이름을*]

## <a name="arguments"></a>인수

*name*<br/>
컴파일러를 통해 생성 되는.xdc 파일의 이름입니다. 하나의.cpp 파일은 컴파일에서 전달 될 때만 유효 합니다.

## <a name="remarks"></a>설명

.Xdc 파일 xdcmake.exe 사용 하 여.xml 파일로 처리 됩니다. 자세한 내용은 [XDCMake 참조](../../ide/xdcmake-reference.md)합니다.

소스 코드 파일에 문서 주석을 추가할 수 있습니다. 자세한 내용은 [Tags for Documentation Comments 권장](../../ide/recommended-tags-for-documentation-comments-visual-cpp.md)합니다.

IntelliSense를 사용 하 여 생성 된.xml 파일을 사용 하려면 지원 및.xml 파일을 저장 하려는 어셈블리와 동일한 어셈블리와 동일한 디렉터리에.xml 파일의 파일 이름을 지정 합니다. Visual Studio 프로젝트에서 어셈블리를 참조할 때.xml 파일을 찾을 수도 됩니다. 자세한 내용은 [IntelliSense를 사용 하 여](/visualstudio/ide/using-intellisense) 하 고 [XML 코드 주석 제공](/visualstudio/ide/supplying-xml-code-comments)합니다.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 컴파일러 옵션을 설정하려면

1.  프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. 선택 된 **구성 속성** > **C/c + +** > **출력 파일** 속성 페이지.

1. 수정 된 **XML 문서 파일 생성** 속성입니다.

### <a name="to-set-this-linker-option-programmatically"></a>프로그래밍 방식으로 이 링커 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.GenerateXMLDocumentationFiles%2A>을 참조하세요.

## <a name="see-also"></a>참고 항목

[컴파일러 옵션](../../build/reference/compiler-options.md)   
[컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md)