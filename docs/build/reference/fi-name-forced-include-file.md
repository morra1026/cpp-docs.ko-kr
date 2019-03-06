---
title: /FI(강제 포함 파일 이름 지정)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCNMakeTool.ForcedIncludes
- VC.Project.VCCLCompilerTool.ForcedIncludeFiles
- VC.Project.VCCLWCECompilerTool.ForcedIncludeFiles
- /fi
helpviewer_keywords:
- FI compiler option [C++]
- -FI compiler option [C++]
- /FI compiler option [C++]
- preprocess header file compiler option [C++]
ms.assetid: 07e79577-8152-4df9-a64c-aae08c603397
ms.openlocfilehash: b91ca1ba6cc97157be0ab16fc18e065dc501d5fd
ms.sourcegitcommit: bff17488ac5538b8eaac57156a4d6f06b37d6b7f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57422470"
---
# <a name="fi-name-forced-include-file"></a>/FI(강제 포함 파일 이름 지정)

지정 된 헤더 파일을 처리 하도록 전처리기에 발생 합니다.

## <a name="syntax"></a>구문

```
/FI[ ]pathname
```

## <a name="remarks"></a>설명

이 옵션에 큰따옴표를 사용 하 여 파일을 지정 하는 것과 동일한 효과가 `#include` 명령줄 CL 환경 변수 또는 명령 파일에 지정 된 모든 소스 파일의 첫 번째 줄에서 지시문입니다. 여러 개 사용 하면 **/FI** 옵션 파일 CL에 의해 처리 된 순서 대로 포함 됩니다.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 컴파일러 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. **C/C++** 폴더를 클릭합니다.

1. 클릭 합니다 **고급** 속성 페이지.

1. 수정 된 **강제 포함** 속성입니다.

### <a name="to-set-this-compiler-option-programmatically"></a>프로그래밍 방식으로 이 컴파일러 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.ForcedIncludeFiles%2A>을 참조하세요.

## <a name="see-also"></a>참고자료

[출력 파일(/F) 옵션](../../build/reference/output-file-f-options.md)<br/>
[컴파일러 옵션](../../build/reference/compiler-options.md)<br/>
[컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md)<br/>
[경로 이름 지정](../../build/reference/specifying-the-pathname.md)
