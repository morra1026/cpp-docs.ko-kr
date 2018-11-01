---
title: /Fo(개체 파일 이름)
ms.date: 11/04/2016
f1_keywords:
- /Fo
- VC.Project.VCCLCompilerTool.ObjectFile
- VC.Project.VCCLWCECompilerTool.ObjectFile
helpviewer_keywords:
- Fo compiler option [C++]
- object files, naming
- /Fo compiler option [C++]
- -Fo compiler option [C++]
ms.assetid: 0e6d593e-4e7f-4990-9e6e-92e1dcbcf6e6
ms.openlocfilehash: 19e84cbb1be53c8e1a7ae32b6ea2fc3ceeb2edae
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50640338"
---
# <a name="fo-object-file-name"></a>/Fo(개체 파일 이름)

기본값 대신 사용할 개체(.obj) 파일 이름 또는 디렉터리를 지정합니다.

## <a name="syntax"></a>구문

```
/Fopathname
```

## <a name="remarks"></a>설명

이 옵션을 사용 하지 않는 경우 개체 파일을 소스 파일 및.obj 확장의 기본 이름을 사용 합니다. 다른 이름 및 원하는 확장을 사용할 수 있지만 권장 되는 규칙을 사용 하는 것입니다. obj.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 컴파일러 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. **C/C++** 폴더를 클릭합니다.

1. **출력 파일** 속성 페이지를 클릭합니다.

1. 수정 된 **개체 파일 이름을** 속성입니다.  개발 환경 개체 파일의 확장명이 있어야 합니다. obj.

### <a name="to-set-this-compiler-option-programmatically"></a>프로그래밍 방식으로 이 컴파일러 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.ObjectFile%2A>을 참조하세요.

## <a name="example"></a>예제

다음 명령줄 프로그램 기존 디렉터리에 \OBJECT, B. 드라이브 THIS.obj 라는 개체 파일을 만듭니다.

```
CL /FoB:\OBJECT\ THIS.C
```

## <a name="see-also"></a>참고 항목

[출력 파일(/F) 옵션](../../build/reference/output-file-f-options.md)<br/>
[컴파일러 옵션](../../build/reference/compiler-options.md)<br/>
[컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md)<br/>
[경로 이름 지정](../../build/reference/specifying-the-pathname.md)