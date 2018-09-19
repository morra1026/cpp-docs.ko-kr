---
title: -Gm (최소 다시 빌드 사용) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- VC.Project.VCCLCompilerTool.MinimalRebuild
- /Gm
- /FD
- VC.Project.VCCLWCECompilerTool.MinimalRebuild
dev_langs:
- C++
helpviewer_keywords:
- /Gm compiler option [C++]
- minimal rebuild
- enable minimal rebuild compiler option [C++]
- Gm compiler option [C++]
- -Gm compiler option [C++]
ms.assetid: d8869ce0-d2ea-40eb-8dae-6d2cdb61dd59
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 0f18881e79a3f82941f04dccbde210b2c62dcbca
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45725766"
---
# <a name="gm-enable-minimal-rebuild"></a>/Gm(최소 다시 빌드 사용)

변경된 C++ 클래스 정의(헤더 파일(.h)에 저장됨)가 포함된 C++ 소스 파일을 다시 컴파일해야 할지 여부를 결정하는 최소 다시 빌드가 가능하도록 설정합니다.

## <a name="syntax"></a>구문

```
/Gm
```

## <a name="remarks"></a>설명

컴파일러는 첫 번째 컴파일 중 소스 파일과 .idb 파일의 클래스 정의 간의 종속성 정보를 저장합니다. (종속성 정보에서는 어떤 클래스 정의 종속 된 소스 파일 및에 어떤.h 파일을 정의 합니다.) 수정된 된.h 파일이 포함 된 경우에 소스 파일을 컴파일하고 해야 하는지 여부를 확인 하려면.idb 파일에 저장 된 정보를 사용 하는 후속 컴파일합니다.

> [!NOTE]
>  최소 다시 빌드는 포함 파일 간에 변경되지 않는 클래스 정의를 사용합니다. .idb 파일의 종속성 정보는 전체 프로젝트에 대해 생성되므로 클래스 정의는 프로젝트에 대해 전역적이어야 합니다(지정된 클래스에 대해서는 정의가 하나만 있어야 함). 프로젝트에 클래스 정의가 두 개 이상 있는 경우 최소 다시 빌드를 사용하지 마세요.

Incremental linker를 사용 하 여.obj 파일에 포함 된 Windows 메타 데이터를 지원 하지 않으므로 합니다 [/ZW (Windows 런타임 컴파일)](../../build/reference/zw-windows-runtime-compilation.md) 옵션을 합니다 **/Gm** 옵션이 호환 되지 않습니다.  **/ZW**합니다.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 컴파일러 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. **C/C++** 폴더를 클릭합니다.

1. 클릭 합니다 **코드 생성** 속성 페이지.

1. 수정 된 **최소 다시 빌드** 속성입니다.

### <a name="to-set-this-compiler-option-programmatically"></a>프로그래밍 방식으로 이 컴파일러 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.MinimalRebuild%2A>을 참조하세요.

## <a name="see-also"></a>참고 항목

[컴파일러 옵션](../../build/reference/compiler-options.md)<br/>
[컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md)