---
title: -WL (한 줄 진단 사용 하도록 설정) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- /wl
dev_langs:
- C++
helpviewer_keywords:
- -WL compiler option [C++]
- /WL compiler option [C++]
- WL compiler option [C++]
ms.assetid: 332cadb4-8ea6-45fe-b67d-33ddec1f2c2e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: e82a3273673d45d1abf3ac201d7a0f63334cecbb
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45718674"
---
# <a name="wl-enable-one-line-diagnostics"></a>/WL(1줄 진단 사용)

오류 또는 경고 메시지에 추가 정보를 추가합니다.

## <a name="syntax"></a>구문

```
/WL
```

## <a name="remarks"></a>설명

오류 및 c + + 컴파일러에서 경고 메시지는 기본적으로 새 줄에 표시 되는 추가 정보도 올 수 있습니다. 명령줄에서 컴파일할 때 오류 또는 경고 메시지에 정보 추가 줄을 추가할 수 있습니다. 이 로그 파일에 빌드 출력을 캡처하고 다음 모든 오류 및 경고를 확인 하려면 해당 로그를 처리 하는 경우이 바람직 할 수 있습니다. 세미콜론 추가 줄에서 오류 또는 경고 메시지가 구분 됩니다.

일부 오류 및 경고 메시지에 정보의 줄을 경우 다음 코드에서 추가 정보를 줄 수 있는 오류를 생성 합니다. 사용 하는 경우의 효과 테스트할 수 있습니다 **/WL**합니다.

```
// compiler_option_WL.cpp
// compile with: /WL
#include <queue>
int main() {
   std::queue<int> q;
   q.fromthecontinuum();   // C2039
}
```

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