---
title: /ASSEMBLYDEBUG(DebuggableAttribute 추가)
ms.date: 11/04/2016
f1_keywords:
- VC.Project.VCLinkerTool.AssemblyDebug
- /ASSEMBLYDEBUG
helpviewer_keywords:
- /ASSEMBLYDEBUG linker option
- -ASSEMBLYDEBUG linker option
- ASSEMBLYDEBUG linker option
ms.assetid: 94443af3-470c-41d7-83a0-7434563d7982
ms.openlocfilehash: 7e0a2133549a72fa747c67b40f9de1f8f48362b7
ms.sourcegitcommit: bff17488ac5538b8eaac57156a4d6f06b37d6b7f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57426539"
---
# <a name="assemblydebug-add-debuggableattribute"></a>/ASSEMBLYDEBUG(DebuggableAttribute 추가)

```
/ASSEMBLYDEBUG[:DISABLE]
```

/ASSEMBLYDEBUG 내보냅니다 합니다 **DebuggableAttribute** 디버그 정보 추적 및 사용 하지 않도록 설정 JIT 최적화를 사용 하 여 특성입니다. 원본에서 다음 특성을 지정 하는 것 같습니다.

```
[assembly:Debuggable(true, true)];   // same as /ASSEMBLYDEBUG
```

/Assemblydebug: disable 내보냅니다 합니다 **DebuggableAttribute** 특성 디버그 정보 추적을 사용 하지 않도록 설정 하지만 및 JIT 최적화를 활성화 합니다. 원본에서 다음 특성을 지정 하는 것 같습니다.

```
[assembly:Debuggable(false, false)];   // same as /ASSEMBLYDEBUG:DISABLE
```

기본적으로 내보내지 합니다 **DebuggableAttribute** 특성입니다.

DebuggableAttribute 소스 코드에서 직접 어셈블리에도 추가할 수 있습니다. 예를 들면 다음과 같습니다.

```
[assembly:Debuggable(true, true)];   // same as /ASSEMBLYDEBUG
```

## <a name="remarks"></a>설명

명시적으로 관리 되는 이미지를 디버깅할 수 있는지를 지정 하는 것이 반드시 합니다. 사용 하 여 [/Zi](../../build/reference/z7-zi-zi-debug-information-format.md) 만으로는 충분 하지 않습니다.

어셈블리 생성에 영향을 주는 링커 옵션도 있습니다.

- [/ASSEMBLYLINKRESOURCE](../../build/reference/assemblylinkresource-link-to-dotnet-framework-resource.md)

- [/ASSEMBLYMODULE](../../build/reference/assemblymodule-add-a-msil-module-to-the-assembly.md)

- [/ASSEMBLYRESOURCE](../../build/reference/assemblyresource-embed-a-managed-resource.md)

- [/DELAYSIGN](../../build/reference/delaysign-partially-sign-an-assembly.md)

- [/KEYCONTAINER](../../build/reference/keycontainer-specify-a-key-container-to-sign-an-assembly.md)

- [/KEYFILE](../../build/reference/keyfile-specify-key-or-key-pair-to-sign-an-assembly.md)

- [/NOASSEMBLY](../../build/reference/noassembly-create-a-msil-module.md)

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 링커 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 참조 하세요 [Visual c + + 프로젝트 속성 설정](../../ide/working-with-project-properties.md)합니다.

1. 클릭 합니다 **링커** 폴더입니다.

1. 클릭 합니다 **디버그** 속성 페이지.

1. 수정 된 **디버깅 가능한 어셈블리** 속성입니다.

### <a name="to-set-this-linker-option-programmatically"></a>프로그래밍 방식으로 이 링커 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.AssemblyDebug%2A>을 참조하세요.

## <a name="see-also"></a>참고자료

[링커 옵션 설정](../../build/reference/setting-linker-options.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)
