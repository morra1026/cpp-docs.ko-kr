---
title: -Y-(미리 컴파일된 헤더 옵션 무시) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- /y-
dev_langs:
- C++
helpviewer_keywords:
- Y- compiler option [C++]
- -Y- compiler option [C++]
- /Y- compiler option [C++]
ms.assetid: cfaecb36-58db-46b8-b04d-cca6072b1b7a
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d99408490874f989a5063aef29d0b0e020f2e08a
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45719656"
---
# <a name="y--ignore-precompiled-header-options"></a>/Y-(미리 컴파일된 헤더 옵션 무시)

다른 모든 `/Y` 컴파일러 옵션을 무시과 자체를 재정의할 수 없습니다.

## <a name="syntax"></a>구문

```
/Y-
```

## <a name="remarks"></a>설명

미리 컴파일된 헤더에 대 한 자세한 내용은 다음을 참조 하세요.

- [/Y(미리 컴파일된 헤더)](../../build/reference/y-precompiled-headers.md)

- [미리 컴파일된 헤더 파일 만들기](../../build/reference/creating-precompiled-header-files.md)

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 컴파일러 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. **C/C++** 폴더를 클릭합니다.

1. **명령줄** 속성 페이지를 클릭합니다.

1. **추가 옵션** 상자에 컴파일러 옵션을 입력합니다.

### <a name="to-set-this-compiler-option-programmatically"></a>프로그래밍 방식으로 이 컴파일러 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions%2A>을 참조하세요.

## <a name="see-also"></a>참고 항목

[컴파일러 옵션](../../build/reference/compiler-options.md)<br/>
[컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md)