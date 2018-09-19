---
title: -MANIFESTUAC (매니페스트에 UAC 포함 정보) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- VC.Project.VCLinkerTool.UACUIAccess
- VC.Project.VCLinkerTool.UACExecutionLevel
- VC.Project.VCLinkerTool.EnableUAC
dev_langs:
- C++
helpviewer_keywords:
- /MANIFESTUAC linker option
- MANIFESTUAC linker option
- -MANIFESTUAC linker option
ms.assetid: 2d243c39-fa13-493c-b56f-d0d972a1603a
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 1b3997f8beb414992464c51ca1c1fd944145c43d
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45715145"
---
# <a name="manifestuac-embeds-uac-information-in-manifest"></a>/MANIFESTUAC(매니페스트에 UAC 정보 포함)

UAC(사용자 계정 컨트롤) 정보를 program 매니페스트에 포함할지 여부를 지정합니다.

## <a name="syntax"></a>구문

```
/MANIFESTUAC
/MANIFESTUAC:NO
/MANIFESTUAC:fragment
/MANIFESTUAC:level=_level
/MANIFESTUAC:uiAccess=_uiAccess
```

### <a name="parameters"></a>매개 변수

*조각*<br/>
포함 된 문자열을 `level` 및 `uiAccess` 값입니다. 자세한 내용은이 항목의 뒷부분에 나오는 주의 섹션을 참조 하세요.

*수준 (_l)*<br/>
중 하나 *asInvoker*하십시오 *highestAvailable*, 또는 *requireAdministrator*합니다. AsInvoker 기본값은입니다. 자세한 내용은이 항목의 뒷부분에 나오는 주의 섹션을 참조 하세요.

*_uiAccess*<br/>
응용 프로그램에서 사용자 인터페이스 보호 수준을 우회하고 데스크톱에서 상위 권한 창에 입력할 수 있게 하려면 `true`이고 그렇지 않으면 `false`입니다. 기본값은 `false`입니다. 로 `true` 사용자 인터페이스 접근성 응용 프로그램에 대해서만 합니다.

## <a name="remarks"></a>설명

명령줄에서 여러 /MANIFESTUAC 옵션을 지정 하는 경우 입력 한 개가 우선적으로 적용 합니다.

/MANIFESTUAC:level에 대 한 선택 항목은 다음과 같습니다.

- `asInvoker`: 응용 프로그램을 시작한 프로세스와 동일한 권한으로 실행 됩니다. 응용 프로그램을 선택 하 여 높은 권한 수준으로 승격할 수도 있습니다 **관리자 권한으로 실행**합니다.

- highestAvailable: 응용 프로그램 수는 가장 높은 권한 수준으로 실행 됩니다. 응용 프로그램을 시작한 사용자가 Administrators 그룹의 멤버인 경우이 옵션은 requireAdministrator 동일 합니다. 가장 높은 사용 가능한 사용 권한 수준이 열기 프로세스의 수준 보다 높은 경우 시스템 자격 증명을 묻는 됩니다.

- requireAdministrator: 응용 프로그램 관리자 권한으로 실행 됩니다. 응용 프로그램을 시작 하는 사용자는 Administrators 그룹의 구성원 이어야 합니다. 열기 프로세스를 관리자 권한으로 실행 하지 않는 경우 시스템 자격 증명을 묻는 됩니다.

/MANIFESTUAC:fragment 옵션을 사용 하 여 한 번에 수준 및 uiAccess 값을 지정할 수 있습니다. 조각 다음 형식 이어야 합니다.

```
"level=[ asInvoker | highestAvailable | requireAdministrator ] uiAccess=[ true | false ]"
```

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 링커 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. **구성 속성** 노드를 확장합니다.

1. 확장 된 **링커** 노드.

1. 선택 된 **매니페스트 파일** 속성 페이지.

1. 수정 된 **사용 사용자 계정 컨트롤 (UAC)** 를 **UAC 실행 수준**, 및 **UAC UI 보호 건너뛰기** 속성입니다.

### <a name="to-set-this-linker-option-programmatically"></a>프로그래밍 방식으로 이 링커 옵션을 설정하려면

1. See <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.EnableUAC%2A>, <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.UACExecutionLevel%2A> 및 <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.UACUIAccess%2A>을 참조하십시오.

## <a name="see-also"></a>참고 항목

[링커 옵션 설정](../../build/reference/setting-linker-options.md)<br/>
[링커 옵션](../../build/reference/linker-options.md)