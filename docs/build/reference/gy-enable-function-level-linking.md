---
title: -Gy (함수 수준 링크 사용) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- VC.Project.VCCLCompilerTool.EnableFunctionLevelLinking
- /gy
- VC.Project.VCCLWCECompilerTool.EnableFunctionLevelLinking
dev_langs:
- C++
helpviewer_keywords:
- enable function-level linking compiler option [C++]
- COMDAT function
- Gy compiler option [C++]
- -Gy compiler option [C++]
- /Gy compiler option [C++]
- packaged functions
ms.assetid: 0d3cf14c-ed7d-4ad3-b4b6-104e56f61046
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 09faa1a1d2b6743b7fce31af32ba4fe1572b592e
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45705005"
---
# <a name="gy-enable-function-level-linking"></a>/Gy(함수 수준 링크 사용)

컴파일러가 개별 함수를 패키지된 함수(COMDAT)의 형태로 패키지할 수 있게 합니다.

## <a name="syntax"></a>구문

```
/Gy[-]
```

## <a name="remarks"></a>설명

링커에서 함수를 제외 하거나 DLL 또는.exe 파일의 개별 함수를 정렬 하는 Comdat로 별도로 패키지 수 있습니다.

링커 옵션을 사용할 수 있습니다 [/OPT (최적화)](../../build/reference/opt-optimizations.md) .exe 파일에서 참조 되지 않은 패키지에 포함 된 함수를 제외 합니다.

링커 옵션을 사용할 수 있습니다 [/ORDER (Put 함수에 순서 지정)](../../build/reference/order-put-functions-in-order.md) .exe 파일에 지정된 된 순서에 패키지 된 함수를 포함 합니다.

인라인 함수는 호출으로 인스턴스화되는 경우 항상 패키지로 (있는 경우, 예를 들어, 인라인 off 인지 함수 주소를 사용). 또한 클래스 선언에 정의 된 c + + 멤버 함수는 자동으로 패키지; 다른 함수 되지 않으며 패키지 함수로 컴파일하기 위해 반드시이 옵션을 선택 합니다.

> [!NOTE]
>  합니다 [/ZI](../../build/reference/z7-zi-zi-debug-information-format.md) 편집 하며 계속 하기를 사용 하는 옵션을 자동으로 설정 합니다 **/Gy** 옵션입니다.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 컴파일러 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. **C/C++** 폴더를 클릭합니다.

1. 클릭 합니다 **코드 생성** 속성 페이지.

1. 수정 된 **함수 수준 링크 사용** 속성입니다.

### <a name="to-set-this-compiler-option-programmatically"></a>프로그래밍 방식으로 이 컴파일러 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.EnableFunctionLevelLinking%2A>을 참조하세요.

## <a name="see-also"></a>참고 항목

[컴파일러 옵션](../../build/reference/compiler-options.md)<br/>
[컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md)