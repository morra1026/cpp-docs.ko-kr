---
title: /link(옵션을 링커로 전달)
ms.date: 11/04/2016
f1_keywords:
- /link
helpviewer_keywords:
- /link compiler option [C++]
- pass options to linker
- link compiler option [C++]
- linker [C++], passing options to
- -link compiler option [C++]
- cl.exe compiler [C++], passing options to linker
ms.assetid: 16902a94-c094-4328-841f-3ac94ca04848
ms.openlocfilehash: dfa39988782a0c5bd121b6e18402d3f6b67a13e9
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50574930"
---
# <a name="link-pass-options-to-linker"></a>/link(옵션을 링커로 전달)

하나 이상의 링커 옵션을 링커에 전달 합니다.

## <a name="syntax"></a>구문

```
/link linkeroptions
```

## <a name="arguments"></a>인수

*linkeroptions*<br/>
링커 옵션을 링커로 전달 될 옵션을 합니다.

## <a name="remarks"></a>설명

합니다 **/l i n** 옵션 및 링커 옵션으로 모든 파일 이름 및 CL 옵션 뒤에 나타나야 합니다. 사이 공백을 않습니다 **/l i n** 고 `linkeroptions`입니다. 자세한 내용은 [링커 옵션 설정](../../build/reference/setting-linker-options.md)합니다.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 컴파일러 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. 클릭 합니다 **링커** 폴더입니다.

1. 링커 속성 페이지를 클릭 합니다.

1. 하나 이상의 속성을 수정 합니다.

### <a name="to-set-this-compiler-option-programmatically"></a>프로그래밍 방식으로 이 컴파일러 옵션을 설정하려면

- 이 컴파일러 옵션을 프로그래밍 방식으로 변경할 수 없습니다.

## <a name="see-also"></a>참고 항목

[컴파일러 옵션](../../build/reference/compiler-options.md)<br/>
[컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md)