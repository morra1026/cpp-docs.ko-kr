---
title: -I (추가 포함 디렉터리) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- VC.Project.VCCLWCECompilerTool.AdditionalIncludeDirectories
- VC.Project.VCCLCompilerTool.AdditionalIncludeDirectories
- /I
- VC.Project.VCNMakeTool.IncludeSearchPath
dev_langs:
- C++
helpviewer_keywords:
- /I compiler option [C++]
- Additional Include Directories compiler option
- I compiler option [C++]
- -I compiler option [C++]
- set include directories
- include directories, compiler option [C++]
ms.assetid: 3e9add2a-5ed8-4d15-ad79-5b411e313a49
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 506f0900cfc7ef5f84e11b2c76d4b593f81d10ba
ms.sourcegitcommit: 761c5f7c506915f5a62ef3847714f43e9b815352
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44109086"
---
# <a name="i-additional-include-directories"></a>/I(추가 포함 디렉터리)
포함 파일을 검색할 디렉터리 목록에 디렉터리를 추가 합니다.

## <a name="syntax"></a>구문

```  
/I[ ]directory
```  

## <a name="arguments"></a>인수
*디렉터리*<br/>
디렉터리 목록에 추가할 디렉터리는 include 파일 검색 합니다.

## <a name="remarks"></a>설명
둘 이상의 디렉터리를 추가 하려면이 옵션을 두 번 이상 사용 합니다. 지정된 된 include 파일을 찾을 때까지만 디렉터리가 검색 됩니다.

표준 포함 경로 무시를 사용 하 여이 옵션을 사용할 수 있습니다 ([/X (표준 포함 경로 무시)](../../build/reference/x-ignore-standard-include-paths.md)) 옵션입니다.

컴파일러는 다음 순서 대로 디렉터리에 대 한 검색합니다.

1.  원본 파일이 포함 된 디렉터리입니다.

2.  로 지정 된 디렉터리를 **/I** CL에서 하는 순서로 옵션입니다.

3.  에 지정 된 디렉터리를 **INCLUDE** 환경 변수입니다.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 컴파일러 옵션을 설정하려면

1.  프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

2.  **C/C++** 폴더를 클릭합니다.

3.  클릭 합니다 **일반** 속성 페이지.

4.  수정 된 **Additional Include Directories** 속성입니다.

### <a name="to-set-this-compiler-option-programmatically"></a>프로그래밍 방식으로 이 컴파일러 옵션을 설정하려면

-   <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalIncludeDirectories%2A>을 참조하세요.

## <a name="example"></a>예제
다음 명령을 다음 순서 대로 MAIN.c 요청한 포함 파일을 찾습니다: \INCLUDE 디렉터리에 다음 \MY\INCLUDE 디렉터리에서 다음 MAIN.c를 포함 하 고 마지막 디렉터리에 할당할 포함 되는 디렉터리의 첫 번째 환경 변수입니다.

```  
CL /I \INCLUDE /I\MY\INCLUDE MAIN.C
```  

## <a name="see-also"></a>참고 항목
[컴파일러 옵션](../../build/reference/compiler-options.md)   
[컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md)