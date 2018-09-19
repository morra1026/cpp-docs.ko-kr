---
title: -Yc (미리 컴파일된 헤더 파일 만들기) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- devlang-cpp
ms.topic: reference
f1_keywords:
- VC.Project.VCCLCompilerTool.UsePrecompiledHeader
- /yc
- VC.Project.VCCLWCECompilerTool.PrecompiledHeaderThrough
- VC.Project.VCCLWCECompilerTool.UsePrecompiledHeader
- VC.Project.VCCLCompilerTool.PrecompiledHeaderThrough
dev_langs:
- C++
helpviewer_keywords:
- precompiled header files, creating
- PCH files, creating
- .pch files, creating
- -Yc compiler option [C++]
- /Yc compiler option [C++]
- Yc compiler option [C++]
ms.assetid: 47c2e555-b4f5-46e6-906e-ab5cf21f0678
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c5288e748956a405073697ddd7331a73b95d8650
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45714248"
---
# <a name="yc-create-precompiled-header-file"></a>/Yc(미리 컴파일된 헤더 파일 만들기)

특정 시점에 컴파일 상태를 나타내는 미리 컴파일된 헤더 (.pch) 파일을 만드는 컴파일러에 지시 합니다.

## <a name="syntax"></a>구문

> __/Yc__
>  __/Yc__*파일 이름*

## <a name="arguments"></a>인수

*filename*<br/>
헤더 (.h) 파일을 지정합니다. 이 인수를 사용 하는 경우 컴파일러는.h 파일을 포함 하는 모든 코드를 컴파일합니다.

## <a name="remarks"></a>설명

때 **/Yc** 컴파일러는 기본 소스 파일 또는 기본 파일에서 끝까지 모든 코드를 컴파일하는 인수 없이 지정 된 위치를 [hdrstop](../../preprocessor/hdrstop.md) 지시문 발생 합니다. 결과.pch 파일 이름이 동일한 기본 기본 소스 파일을 사용 하 여 다른 파일 이름을 지정 하지 않으면 합니다 **hdrstop** pragma와 **/Fp** 옵션입니다.

미리 컴파일된 코드는 지정 된 파일의 기본 이름에서 만든 이름으로 파일에 저장 합니다 **/Yc** 옵션과 확장명이.pch 합니다. 사용할 수도 있습니다는 [/Fp (이름입니다. Pch 파일)](../../build/reference/fp-name-dot-pch-file.md) 미리 컴파일된 헤더 파일의 이름을 지정 하는 옵션입니다.

사용 하는 경우 __/Yc__*filename*, 컴파일러 및 후속 사용에 대 한 지정된 된 파일까지 모든 코드를 컴파일합니다 합니다 [/Yu (미리 컴파일된 헤더 파일 사용)](../../build/reference/yu-use-precompiled-header-file.md) 옵션입니다.

경우 옵션 __/Yc__*filename* 하 고 __/Yu__*filename* 동일한 명령줄에서 발생 하 고 참조 하거나 파일 이름이 암시 하는 둘 다 __/Yc__*filename* 우선적으로 적용 합니다. 이 기능은 메이크파일 작성을 단순화 합니다.

미리 컴파일된 헤더에 대 한 자세한 내용은 다음을 참조 하세요.

- [/Y(미리 컴파일된 헤더)](../../build/reference/y-precompiled-headers.md)

- [미리 컴파일된 헤더 파일 만들기](../../build/reference/creating-precompiled-header-files.md)

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 컴파일러 옵션을 설정하려면

1. .Cpp 파일을 선택 합니다. .Cpp 파일은 #include 미리 컴파일된 헤더 정보가 포함 된.h 파일입니다. 프로젝트의 **/Yc** 설정은 파일 수준에서 재정의할 수 있습니다.

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. 엽니다는 **구성 속성**를 **C/c + +** 를 **미리 컴파일된 헤더** 속성 페이지.

1. 수정 된 **미리 컴파일된 헤더** 속성입니다.

1. 파일을 설정 하려면 다음을 수정 합니다 **미리 컴파일된 헤더 파일** 속성입니다.

### <a name="to-set-this-compiler-option-programmatically"></a>프로그래밍 방식으로 이 컴파일러 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.PrecompiledHeaderThrough%2A> 및 <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.UsePrecompiledHeader%2A>을 참조하십시오.

## <a name="example"></a>예제

다음 코드를 살펴보세요.

```cpp
// prog.cpp
// compile with: cl /c /Ycmyapp.h prog.cpp
#include <afxwin.h>   // Include header for class library
#include "resource.h" // Include resource definitions
#include "myapp.h"    // Include information specific to this app
// ...
```

명령을 사용 하 여이 코드를 컴파일할 때 `CL /YcMYAPP.H PROG.CPP`, 컴파일러 AFXWIN.h, RESOURCE.h에 대 한 모든 전처리를 저장 하 고 미리 컴파일된 헤더 파일에 MYAPP.h MYAPP.pch를 호출 합니다.

## <a name="see-also"></a>참고 항목

[컴파일러 옵션](../../build/reference/compiler-options.md)<br/>
[컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md)<br/>
[미리 컴파일된 헤더 파일 만들기](../../build/reference/creating-precompiled-header-files.md)