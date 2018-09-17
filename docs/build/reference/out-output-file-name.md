---
title: -OUT (출력 파일 이름) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- VC.Project.VCLinkerTool.OutputFile
- /out
dev_langs:
- C++
helpviewer_keywords:
- output files, name linker option
- -OUT linker option
- OUT linker option
- /OUT C++ linker option
- linker [C++], output files
ms.assetid: 976210a4-e51f-4cfb-af5e-c16344455834
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 8c4bfc79a257424820bed5f784cb0a83daf016d5
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45725402"
---
# <a name="out-output-file-name"></a>/OUT(출력 파일 이름)

```
/OUT:filename
```

## <a name="arguments"></a>인수

*filename*<br/>
출력 파일에 대 한 사용자 지정 이름입니다. 기본 이름을 대체합니다.

## <a name="remarks"></a>설명

/OUT 옵션은 링커가 만드는 프로그램의 위치와 기본 이름을 재정의 합니다.

기본적으로 링커는 지정 된 첫 번째.obj 파일 (.exe 또는.dll) 해당 확장의 기본 이름을 사용 하 여 파일 이름을 형성 합니다.

이 옵션은 기본 이름을.mapfile 또는 가져오기 라이브러리에 대 한 합니다. 자세한 내용은 참조 하세요 [맵 파일 생성](../../build/reference/map-generate-mapfile.md) (/map) 및 [/IMPLIB](../../build/reference/implib-name-import-library.md)합니다.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 링커 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 참조 하세요 [Visual c + + 프로젝트 속성 설정](../../ide/working-with-project-properties.md)합니다.

1. 클릭 합니다 **링커** 폴더입니다.

1. 클릭 합니다 **일반** 속성 페이지.

1. 수정 된 **출력 파일** 속성입니다.

### <a name="to-set-this-linker-option-programmatically"></a>프로그래밍 방식으로 이 링커 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.OutputFile%2A>을 참조하세요.

## <a name="see-also"></a>참고 항목

[링커 옵션 설정](../../build/reference/setting-linker-options.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)