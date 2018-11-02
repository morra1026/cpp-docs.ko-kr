---
title: /GR(런타임 형식 정보 사용)
ms.date: 11/04/2016
f1_keywords:
- /gr
- VC.Project.VCCLWCECompilerTool.RuntimeTypeInfo
- VC.Project.VCCLCompilerTool.RuntimeTypeInfo
helpviewer_keywords:
- -Gr compiler option [C++]
- Gr compiler option [C++]
- RTTI compiler option
- /Gr compiler option [C++]
- enable run-time type information compiler option [C++]
ms.assetid: d1f9f850-dcec-49fd-96ef-e72d01148906
ms.openlocfilehash: b0b618b1018912f1cf0172fc461ac2849c4faf5d
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50579350"
---
# <a name="gr-enable-run-time-type-information"></a>/GR(런타임 형식 정보 사용)

런타임 시 개체 형식을 검사 하는 코드를 추가 합니다.

## <a name="syntax"></a>구문

```
/GR[-]
```

## <a name="remarks"></a>설명

때 **/GR** 켜져 컴파일러는 정의 `_CPPRTTI` 전처리기 매크로입니다. 기본적으로 **/GR** 켜져 있습니다. **/ Gr-** 런타임 형식 정보를 사용 하지 않도록 설정 합니다.

사용 하 여 **/GR** 경우 컴파일러는 코드에서 개체 유형을 정적으로 확인할 수 없습니다. 일반적으로 필요 합니다 **/GR** 코드를 사용 하는 경우 옵션 [dynamic_cast Operator](../../cpp/dynamic-cast-operator.md) 또는 [typeid](../../cpp/typeid-operator.md)합니다. 그러나 **/GR** .rdata 섹션 이미지의 크기를 늘립니다. 코드를 사용 하지 않는 경우 **dynamic_cast** 또는 **typeid**하십시오 **/gr-** 작은 이미지를 생성할 수 있습니다.

런타임 형식 검사 하는 방법에 대 한 자세한 내용은 참조 하세요. [런타임 형식 정보](../../cpp/run-time-type-information.md) 에 *c + + 언어 참조*합니다.

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 컴파일러 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. **C/C++** 폴더를 클릭합니다.

1. 클릭 합니다 **언어** 속성 페이지.

1. 수정 된 **런타임 형식 정보 사용** 속성입니다.

### <a name="to-set-this-compiler-option-programmatically"></a>프로그래밍 방식으로 이 컴파일러 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.RuntimeTypeInfo%2A>을 참조하세요.

## <a name="see-also"></a>참고 항목

[컴파일러 옵션](../../build/reference/compiler-options.md)<br/>
[컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md)