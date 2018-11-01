---
title: /arch(ARM)
ms.date: 11/04/2016
ms.assetid: 4f1406ff-f174-487c-a126-8ab06cf447c1
ms.openlocfilehash: bf12abd140a56b1b914156083ecbbd3e61e7285a
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50495573"
---
# <a name="arch-arm"></a>/arch(ARM)

ARM에서 코드 생성 아키텍처를 지정합니다. 참고 항목 [(x86) /arch](../../build/reference/arch-x86.md) 하 고 [(x64) /arch](../../build/reference/arch-x64.md)합니다.

## <a name="syntax"></a>구문

```
/arch:[ARMv7VE|VFPv4]
```

## <a name="arguments"></a>인수

**arch:armv7ve**<br/>
ARMv7VE 가상화 확장명 명령을 사용하도록 설정합니다.

**/ arch:vfpv4**<br/>
ARM VFPv4 명령을 사용하도록 설정합니다. 이 옵션을 지정하지 않으면 VFPv3이 기본값입니다.

## <a name="remarks"></a>설명

`_M_ARM_FP` 매크로 (ARM)에 대 한을 나타내는 경우 **/arch** 컴파일러 옵션 사용. 자세한 내용은 [Predefined Macros](../../preprocessor/predefined-macros.md)을 참조하십시오.

사용 하는 경우 [/clr](../../build/reference/clr-common-language-runtime-compilation.md) 를 컴파일하려면 **/arch** 에 관리 되는 함수에 대 한 코드 생성에 영향을 주지 않습니다. **/arch** 만 코드를 네이티브 함수에 대 한 생성에 영향을 줍니다.

### <a name="to-set-the-archarmv7ve-or-archvfpv4-compiler-option-in-visual-studio"></a>Visual Studio에서 /arch:ARMv7VE 또는 /arch:VFPv4 컴파일러 옵션을 설정하려면

1. 엽니다는 **속성 페이지** 프로젝트에 대 한 대화 상자. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. 선택 된 **C/c + +** 폴더입니다.

1. 선택 된 **명령줄** 속성 페이지.

1. 에 **추가 옵션** 상자에서 추가 `/arch:ARMv7VE` 또는 `/arch:VFPv4`합니다.

### <a name="to-set-this-compiler-option-programmatically"></a>프로그래밍 방식으로 이 컴파일러 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.EnableEnhancedInstructionSet%2A>을 참조하세요.

## <a name="see-also"></a>참고 항목

[/arch(최소 CPU 아키텍처)](../../build/reference/arch-minimum-cpu-architecture.md)<br/>
[컴파일러 옵션](../../build/reference/compiler-options.md)<br/>
[컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md)