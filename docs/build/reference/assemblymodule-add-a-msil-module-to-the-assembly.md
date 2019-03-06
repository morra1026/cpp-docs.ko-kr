---
title: /ASSEMBLYMODULE(MSIL 모듈을 어셈블리에 추가)
ms.date: 11/04/2016
f1_keywords:
- /assemblymodule
- VC.Project.VCLinkerTool.AddModuleNamesToAssembly
helpviewer_keywords:
- ASSEMBLYMODULE linker option
- assemblies [C++], adding modules to
- assemblies [C++]
- /ASSEMBLYMODULE linker option
- -ASSEMBLYMODULE linker option
ms.assetid: 67357da8-e4b6-49fd-932c-329a5777f143
ms.openlocfilehash: 567ec4b1e773e8aa4ff248c7bb110cfb594f089e
ms.sourcegitcommit: bff17488ac5538b8eaac57156a4d6f06b37d6b7f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57416698"
---
# <a name="assemblymodule-add-a-msil-module-to-the-assembly"></a>/ASSEMBLYMODULE(MSIL 모듈을 어셈블리에 추가)

```
/ASSEMBLYMODULE:filename
```

## <a name="arguments"></a>인수

*filename*<br/>
이 어셈블리에 포함 하려는 모듈입니다.

## <a name="remarks"></a>설명

/ASSEMBLYMODULE 옵션을 사용 하면 어셈블리에 대 한 모듈 참조를 추가할 수 있습니다. 모듈의 형식 정보는 모듈 참조를 추가한 어셈블리 프로그램에 사용할 수 없습니다. 그러나 모듈의 형식 정보는 어셈블리를 참조 하는 프로그램에 제공 됩니다.

사용 하 여 [#using](../../preprocessor/hash-using-directive-cpp.md) 을 모두 어셈블리에 대 한 모듈 참조를 추가한 어셈블리 프로그램에 사용할 수 있는 모듈의 형식 정보를 확인 합니다.

예를 들어 다음 시나리오를 고려할 수 있습니다.

1. 사용 하 여 모듈을 만듭니다 [/LN](../../build/reference/ln-create-msil-module.md)합니다.

1. 다른 프로젝트 /ASSEMBLYMODULE를 사용 하 여 어셈블리는 현재 컴파일에서 모듈을 포함 합니다. 이 프로젝트를 사용 하 여 모듈 참조 하지 않으므로 `#using`합니다.

1. 이 어셈블리를 참조 하는 모든 프로젝트 모듈에서 형식도 사용할 이제 수 있습니다.

어셈블리 생성에 영향을 주는 링커 옵션도 있습니다.

- [/ASSEMBLYDEBUG](../../build/reference/assemblydebug-add-debuggableattribute.md)

- [/ASSEMBLYLINKRESOURCE](../../build/reference/assemblylinkresource-link-to-dotnet-framework-resource.md)

- [/ASSEMBLYRESOURCE](../../build/reference/assemblyresource-embed-a-managed-resource.md)

- [/DELAYSIGN](../../build/reference/delaysign-partially-sign-an-assembly.md)

- [/NOASSEMBLY](../../build/reference/noassembly-create-a-msil-module.md)

- [/KEYFILE](../../build/reference/keyfile-specify-key-or-key-pair-to-sign-an-assembly.md)

- [/KEYCONTAINER](../../build/reference/keycontainer-specify-a-key-container-to-sign-an-assembly.md)

Visual C++ 링커는 .netmodule 파일을 입력을 받아들이며, 링커에서 생성된 출력 파일은 링커에 입력된 .netmodules에 대해 런타임 종속성이 없는 어셈블리 또는 .netmodule입니다.  자세한 내용은 [링커 입력 파일로 사용하는 .netmodule 파일](../../build/reference/netmodule-files-as-linker-input.md)을 참조하세요.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 링커 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 참조 하세요 [Visual c + + 프로젝트 속성 설정](../../ide/working-with-project-properties.md)합니다.

1. 클릭 합니다 **링커** 폴더입니다.

1. 클릭 합니다 **입력** 속성 페이지.

1. 수정 된 **어셈블리에 모듈 추가** 속성입니다.

### <a name="to-set-this-linker-option-programmatically"></a>프로그래밍 방식으로 이 링커 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.AddModuleNamesToAssembly%2A>을 참조하세요.

## <a name="see-also"></a>참고자료

[링커 옵션 설정](../../build/reference/setting-linker-options.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)
