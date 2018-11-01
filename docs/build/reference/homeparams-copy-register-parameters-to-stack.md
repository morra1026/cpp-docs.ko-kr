---
title: /homeparams(스택에 레지스터 매개 변수 복사)
ms.date: 11/04/2016
f1_keywords:
- /homeparams
helpviewer_keywords:
- /homeparams compiler option [C++]
- -homeparams compiler option [C++]
ms.assetid: 51067de4-24f7-436b-b8d9-bc867a7d53aa
ms.openlocfilehash: 952a38d2ab1268ee3dc1fda0899a3ba047281b44
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50518458"
---
# <a name="homeparams-copy-register-parameters-to-stack"></a>/homeparams(스택에 레지스터 매개 변수 복사)

레지스터에 전달된 매개 변수를 함수 시작 시 스택의 해당 위치에 기록합니다.

## <a name="syntax"></a>구문

```
/homeparams
```

## <a name="remarks"></a>설명

X64에만이 컴파일러 옵션은 컴파일러 (네이티브 및 크로스 컴파일).

X64에서 매개 변수가 전달 되는 경우 컴파일 호출 규칙에 따라 필요 레지스터에 전달 된 매개 변수에 대해서도 매개 변수에 대 한 합니다. 자세한 내용은 [매개 변수 전달](../../build/parameter-passing.md)합니다. 그러나 릴리스 빌드에서 기본적으로 레지스터 매개 변수는 쓰지 스택에 매개 변수에 대해 이미 제공 된 공간으로. 따라서 프로그램의 최적화 (릴리스) 빌드를 디버그 하기 어렵게 합니다.

릴리스 빌드를 사용 하 여 **/homeparams** 응용 프로그램을 디버깅할 수 있도록 합니다. **/homeparams** 스택에 레지스터 매개 변수를 로드 하기 위한 주기가 필요 하므로 성능 단점이 의미지 않습니다.

디버그 빌드에서 스택의 항상 채워집니다 레지스터에 전달 된 매개 변수입니다.

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