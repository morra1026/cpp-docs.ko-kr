---
title: -AI (메타 데이터 디렉터리 지정) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- VC.Project.VCCLCompilerTool.AdditionalUsingDirectories
- VC.Project.VCNMakeTool.AssemblySearchPath
- /AI
- VC.Project.VCCLWCECompilerTool.AdditionalUsingDirectories
dev_langs:
- C++
helpviewer_keywords:
- /AI compiler option [C++]
- AI compiler option [C++]
- -AI compiler option [C++]
ms.assetid: fb9c1846-504c-4a3b-bb39-c8696de32f6f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ba4cb1411bca452de0f146626421315fa7dc177e
ms.sourcegitcommit: 997e6b7d336cddb388bb6e9e56527725fcaa0624
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2018
ms.locfileid: "48859863"
---
# <a name="ai-specify-metadata-directories"></a>/AI(메타데이터 디렉터리 지정)

`#using` 지시문에 전달된 파일 참조를 확인하기 위해 컴파일러가 검색할 디렉터리를 지정합니다.

## <a name="syntax"></a>구문

> **/AI**_디렉터리_

## <a name="arguments"></a>인수

*디렉터리*<br/>
검색할 컴파일러의 디렉터리나 경로

## <a name="remarks"></a>설명

디렉터리를 하나만 전달할 수는 **/AI** 호출 합니다. 하나를 지정할 **/AI** 컴파일러로 검색 하려는 각 경로 대 한 옵션입니다. 예를 들어에 대 한 컴파일러 검색 경로에 C:\Project\Meta와 C:\Common\Meta를 모두 추가 하려면 `#using` 지시문을 추가 `/AI"C:\Project\Meta" /AI"C:\Common\Meta"` 컴파일러 명령줄에 각 디렉터리를 추가 하거나 합니다 **추가 #using 디렉터리** Visual Studio의 속성입니다.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 컴파일러 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. 선택 된 **구성 속성** > **C/c + +** > **일반** 속성 페이지.

1. 수정 된 **추가 #using 디렉터리** 속성입니다.

### <a name="to-set-this-compiler-option-programmatically"></a>프로그래밍 방식으로 이 컴파일러 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalUsingDirectories%2A>을 참조하세요.

## <a name="see-also"></a>참고 항목

[컴파일러 옵션](../../build/reference/compiler-options.md)<br/>
[컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md)<br/>
[#using 지시문](../../preprocessor/hash-using-directive-cpp.md)
