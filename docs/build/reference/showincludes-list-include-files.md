---
title: -showIncludes (포함 파일 나열) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- VC.Project.VCCLWCECompilerTool.ShowIncludes
- VC.Project.VCCLCompilerTool.ShowIncludes
- /showincludes
dev_langs:
- C++
helpviewer_keywords:
- include files
- /showIncludes compiler option [C++]
- include files, displaying in compilation
- -showIncludes compiler option [C++]
- showIncludes compiler option [C++]
ms.assetid: 0b74b052-f594-45a6-a7c7-09e1a319547d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 51305212f97482c6963ee2ba0d272c5c4692416e
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45709396"
---
# <a name="showincludes-list-include-files"></a>/showIncludes(포함 파일 나열)

컴파일러가 포함 파일의 목록을 출력 합니다. 중첩 된 포함 파일 표시 (포함 된 파일을 포함 하는 파일에서)도 있습니다.

## <a name="syntax"></a>구문

```
/showIncludes
```

## <a name="remarks"></a>설명

포함 파일을 컴파일하는 동안 발생 하는 경우는 메시지가 출력 됩니다. 예를 들어:

```
Note: including file: d:\MyDir\include\stdio.h
```

중첩 된 포함 파일을 들여써서 중첩의 각 수준에 대 한 예를 들어 표시 됩니다.

```
Note: including file: d:\temp\1.h
Note: including file:  d:\temp\2.h
```

이 예에서 `2.h` 내에 포함 된 `1.h`, 따라서 들여쓰기입니다.

합니다 **/showIncludes** 옵션을 내보냅니다 `stderr`아니라 `stdout`합니다.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 컴파일러 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. **C/C++** 폴더를 클릭합니다.

1. 클릭 합니다 **고급** 속성 페이지.

1. 수정 된 **포함 표시** 속성입니다.

### <a name="to-set-this-compiler-option-programmatically"></a>프로그래밍 방식으로 이 컴파일러 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.ShowIncludes%2A>을 참조하세요.

## <a name="see-also"></a>참고 항목

[컴파일러 옵션](../../build/reference/compiler-options.md)<br/>
[컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md)