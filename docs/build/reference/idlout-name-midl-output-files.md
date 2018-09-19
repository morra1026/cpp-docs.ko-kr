---
title: -IDLOUT (MIDL 출력 파일 이름) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- /idlout
- VC.Project.VCLinkerTool.MergedIDLBaseFileName
dev_langs:
- C++
helpviewer_keywords:
- MIDL, output file names
- .idl files, path
- MIDL
- /IDLOUT linker option
- IDL files, path
- -IDLOUT linker option
- IDLOUT linker option
ms.assetid: 10d00a6a-85b4-4de1-8732-e422c6931509
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a6749b59a1c12b5d7c3116a925adc727ad6f7ab5
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45721840"
---
# <a name="idlout-name-midl-output-files"></a>/IDLOUT(MIDL 출력 파일 이름 지정)

```
/IDLOUT:[path\]filename
```

## <a name="parameters"></a>매개 변수

*path*<br/>
절대 또는 상대 경로 지정 합니다. 경로 지정 하 여는.idl 파일의 위치만 변경 다른 모든 파일은 프로젝트 디렉터리에 배치 됩니다.

*filename*<br/>
MIDL 컴파일러에 의해 생성 된.idl 파일의 이름을 지정 합니다. 파일 확장명이 없는 것으로 간주 됩니다. 지정할 *filename*.idl.idl 확장 하려는 경우.

## <a name="remarks"></a>설명

/IDLOUT 옵션은 이름 및.idl 파일의 확장명을 지정합니다.

MIDL 컴파일러가 있는 프로젝트를 연결 하는 경우 Visual c + + 링커에 의해 라고 합니다 [모듈](../../windows/module-cpp.md) 특성입니다.

/IDLOUT은 MIDL 컴파일러와 관련 된 다른 출력 파일의 파일 이름을 지정 합니다.

- *filename*.tlb

- *filename*_p.c

- *filename*_i.c

- *filename*.h

*filename* /IDLOUT에 전달 하는 매개 변수입니다. 하는 경우 [/TLBOUT](../../build/reference/tlbout-name-dot-tlb-file.md) 지정 된 경우.tlb 파일 이름과 /TLBOUT에서 가져오는 *filename*합니다.

/IDLOUT 아니고 /TLBOUT을 지정 하면 링커가 vc70.tlb, vc70.idl, vc70_p.c, vc70_i.c, 및 vc70.h 만듭니다.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 링커 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 참조 하세요 [Visual c + + 프로젝트 속성 설정](../../ide/working-with-project-properties.md)합니다.

1. 클릭 합니다 **링커** 폴더입니다.

1. 클릭 합니다 **포함 IDL** 속성 페이지.

1. 수정 된 **병합 IDL 기본 파일 이름** 속성입니다.

### <a name="to-set-this-linker-option-programmatically"></a>프로그래밍 방식으로 이 링커 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.MergedIDLBaseFileName%2A>을 참조하세요.

## <a name="see-also"></a>참고 항목

[링커 옵션 설정](../../build/reference/setting-linker-options.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)<br/>
[/IGNOREIDL (처리 하지 않음 특성을 MIDL로)](../../build/reference/ignoreidl-don-t-process-attributes-into-midl.md)
[/MIDL (MIDL 명령줄 옵션 지정)](../../build/reference/midl-specify-midl-command-line-options.md)
[특성이 지정 된 프로그램 빌드](../../windows/building-an-attributed-program.md)