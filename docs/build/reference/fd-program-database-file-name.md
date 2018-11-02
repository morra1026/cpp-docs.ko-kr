---
title: /Fd(프로그램 데이터베이스 파일 이름)
ms.date: 11/04/2016
f1_keywords:
- /FD
- VC.Project.VCCLWCECompilerTool.ProgramDataBaseFileName
- VC.Project.VCCLCompilerTool.ProgramDataBaseFileName
helpviewer_keywords:
- /FD compiler option [C++]
- program database file name [C++]
- -FD compiler option [C++]
- PDB files, creating
- program database compiler option [C++]
- .pdb files, creating
- FD compiler option [C++]
ms.assetid: 3977a9ed-f0ac-45df-bf06-01cedd2ba85a
ms.openlocfilehash: 449b0a2be44f438c35feeb446df6d7c47f270c35
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50494319"
---
# <a name="fd-program-database-file-name"></a>/Fd(프로그램 데이터베이스 파일 이름)

만든 프로그램 데이터베이스 (PDB) 파일에 대 한 파일 이름을 지정 [/z7, /Zi, /ZI (디버그 정보 형식)](../../build/reference/z7-zi-zi-debug-information-format.md)합니다.

## <a name="syntax"></a>구문

```
/Fdpathname
```

## <a name="remarks"></a>설명

없이 **/Fd**, PDB 파일 이름을 VC 기본값으로*x*0.pdb, 여기서 *x* 사용 하 여 Visual c + +의 주 버전입니다.

컴파일러 VC 라는.pdb 파일을 만듭니다 (경로가 백슬래시로 끝나는) 파일 이름을 포함 하지 않는 경로 이름을 지정 하는 경우*x*0.pdb 지정된 된 디렉터리에 있습니다.

확장을 포함 하지 않는 파일 이름을 지정 하면 컴파일러는.pdb 확장명으로 사용 합니다.

또한이 옵션은 최소 다시 빌드 및 증분 컴파일을 사용 되는 상태 (.idb) 파일을 이름을 지정 합니다.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 컴파일러 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. **C/C++** 폴더를 클릭합니다.

1. **출력 파일** 속성 페이지를 클릭합니다.

1. 수정 된 **프로그램 데이터베이스 파일 이름** 속성입니다.

### <a name="to-set-this-compiler-option-programmatically"></a>프로그래밍 방식으로 이 컴파일러 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.ProgramDataBaseFileName%2A>을 참조하세요.

## <a name="example"></a>예제

이 명령줄 PROG.pdb 및 PROG.idb 라는.idb 파일 라는.pdb 파일을 만듭니다.

```
CL /DDEBUG /Zi /FdPROG.PDB PROG.CPP
```

## <a name="see-also"></a>참고 항목

[출력 파일(/F) 옵션](../../build/reference/output-file-f-options.md)<br/>
[컴파일러 옵션](../../build/reference/compiler-options.md)<br/>
[컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md)<br/>
[경로 이름 지정](../../build/reference/specifying-the-pathname.md)