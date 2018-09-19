---
title: --(강제 기호 참조)를 포함 하는 중 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- /include
- VC.Project.VCLinkerTool.ForceSymbolReferences
dev_langs:
- C++
helpviewer_keywords:
- INCLUDE linker option
- force symbol references linker option
- symbol references linker force
- /INCLUDE linker option
- symbols, add to symbol table
- -INCLUDE linker option
ms.assetid: 4a039677-360a-480f-bd0b-448e239b449c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 6528f6edc51a2dd01e8f91107827b570a44785de
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45715782"
---
# <a name="include-force-symbol-references"></a>/INCLUDE(강제 기호 참조)

```
/INCLUDE:symbol
```

## <a name="parameters"></a>매개 변수

*기호*<br/>
기호를 기호 테이블을 추가할 수를 지정 합니다.

## <a name="remarks"></a>설명

/INCLUDE 옵션을 사용 하면 링커에서 기호 테이블에 지정된 된 기호를 추가 하려면.

여러 기호를 지정 하려면 쉼표 (,), 세미콜론 (;) 또는 기호 이름 사이 공백을 입력 합니다. 명령줄에서 지정 /INCLUDE:`symbol` 각 기호에 대 한 한 번입니다.

링커 확인 `symbol` 프로그램 기호 정의 포함 하는 개체를 추가 하 여 합니다. 이 기능은 그렇지 않은 경우 링크 되지 프로그램에는 라이브러리 개체를 포함 하는 데 유용 합니다.

이 옵션을 사용 하 여 기호를 지정 하면으로 해당 기호는 제거를 재정의 [/opt: ref](../../build/reference/opt-optimizations.md)합니다.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 링커 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 참조 하세요 [Visual c + + 프로젝트 속성 설정](../../ide/working-with-project-properties.md)합니다.

1. 클릭 합니다 **링커** 폴더입니다.

1. 클릭 합니다 **입력** 속성 페이지.

1. 수정 된 **강제 기호 참조** 속성입니다.

### <a name="to-set-this-linker-option-programmatically"></a>프로그래밍 방식으로 이 링커 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.ForceSymbolReferences%2A>을 참조하세요.

## <a name="see-also"></a>참고 항목

[링커 옵션 설정](../../build/reference/setting-linker-options.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)