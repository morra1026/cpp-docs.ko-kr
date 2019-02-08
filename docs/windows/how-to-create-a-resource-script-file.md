---
title: '방법: 리소스 스크립트 파일 (c + +) 만들기'
ms.date: 11/04/2016
f1_keywords:
- vc.editors.resource
- vc.resvw.add.MFC
helpviewer_keywords:
- rc files [C++], creating
- .rc files [C++], creating
- resource script files [C++], creating
- resources [C++], viewing
- rc files [C++], viewing resources
- .rc files [C++], viewing resources
- resource script files [C++], viewing resources
- resource script files [C++], opening in text format
- .rc files [C++], opening in text format
- rc files [C++], opening in text format
- rc files [C++], adding MFC support
- .rc files [C++], adding MFC support
- MFC, adding support to resource scripts files
- resource script files [C++], adding MFC support
ms.assetid: 82be732a-cdcd-4a58-8de7-976d1418f86b
ms.openlocfilehash: 9055e0f787c238276d3134c2fa6a8afae0102433
ms.sourcegitcommit: 5a7dbd640376e13379f5d5b2cf66c4842e5e737b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55905682"
---
# <a name="how-to-create-a-resource-script-file-c"></a>방법: 리소스 스크립트 파일 (c + +) 만들기

> [!NOTE]
> Express 버전에서는 **리소스 편집기**를 사용할 수 없습니다.
>
> 이 자료는 Windows 데스크톱 애플리케이션에 적용됩니다. .NET 언어의 프로젝트에서는 리소스 스크립트 파일을 사용하지 않습니다. 자세한 내용은 [리소스 파일](../windows/resource-files-visual-studio.md)합니다.

## <a name="to-create-a-new-resource-script-rc-file"></a>새 리소스 스크립트(.rc) 파일을 만들려면

1. **솔루션 탐색기**에 있는 프로젝트 폴더에 포커스를 둡니다. 예를 들면 `MyProject`에 포커스를 둡니다.

   > [!NOTE]
   > **솔루션 탐색기**에 있는 솔루션 폴더 프로젝트 폴더를 혼동하지 마세요. **솔루션** 폴더에 포커스를 둔 경우 **새 항목 추가** 대화 상자를 선택하는 3단계가 다릅니다.

1. **프로젝트** 메뉴에서 **새 항목 추가**를 선택합니다.

1. 에 **새 항목 추가** 대화 상자를 선택 합니다 **Visual c + +** 폴더를 선택 합니다. **리소스 파일 (.rc)** 오른쪽 창에서.

1. 리소스 스크립트 파일에 대 한 이름을 제공 합니다 **이름** 텍스트 상자에서 선택한 **열기**.

이제 .rc 파일을 [생성](../windows/how-to-create-a-resource.md) 하여 새 리소스를 추가할 수 있습니다.

> [!NOTE]
> Visual Studio IDE에 로드된 기존 프로젝트에만 리소스 스크립트(.rc 파일)를 추가할 수 있습니다. 프로젝트의 외부에 독립 실행형 .rc 파일을 만들 수 없습니다. [리소스 템플릿](../windows/how-to-use-resource-templates.md) (.rct 파일)은 언제든지 만들 수 있습니다.

## <a name="to-open-a-resource-script-file-outside-of-a-c-project-standalone"></a>C + + 프로젝트 (독립 실행형) 외부의 리소스 스크립트 파일을 열려면

프로젝트를 열지 않고도 .rc 파일에서 리소스를 볼 수 있습니다. .Rc 파일에서 열리지 않고 문서 창에 열립니다는 [리소스 뷰](../windows/resource-view-window.md) 창 (마찬가지로 파일을 프로젝트 내에서 열려 있을 때).

> [!NOTE]
> 일부 명령은 파일이 프로젝트 외부에서 독립 실행형으로 열릴 때만 사용할 수 있으므로 이는 중요한 차이점입니다. 예를 들어, 저장할 수 있습니다만 파일을 다른 형식으로 또는 다른 파일 이름으로 파일을 프로젝트 외부에서 열릴 때 (합니다 **다른 이름으로 저장** 명령을 사용할 수 없는 프로젝트 내부에서 파일을 열 때).

### <a name="to-open-an-rc-file-outside-a-project"></a>프로젝트 외부에서 .rc 파일을 열려면

1. **파일** 메뉴 선택 **열려**을 선택한 후 **파일**합니다.

1. 에 **열려 있는 파일** 대화 상자에서 보기, 파일을 강조 표시 및 선택 하려는 리소스 스크립트 파일로 이동 **오픈**합니다.

   > [!NOTE]
   > 프로젝트를 먼저 열면 (**파일**를 **엽니다**를 **프로젝트**), 명령도 사용할 수 없습니다. 파일을 "독립 실행형"으로 여는 것은 프로젝트를 먼저 로드하지 않고 파일을 여는 것입니다.

### <a name="to-open-multiple-rc-files-outside-a-project"></a>프로젝트 외부에서 여러 .rc 파일을 열려면

1. 두 리소스 파일을 모두 독립 실행형으로 엽니다. 예를 들어 열 `Source1.rc` 고 `Source2.rc`입니다.

   1. **파일** 메뉴 선택 **열려**을 선택한 후 **파일**합니다.

   1. 에 **파일 열기** 대화 상자에서 열려는 첫 리소스 스크립트 파일로 이동 (`Source1.rc`), 파일을 강조 표시 및 선택 **엽니다**합니다.

   1. 두 번째.rc 파일을 열고 이전 단계를 반복 (`Source2.rc`).

       .rc 파일이 이제 개별 문서 창으로 열려 있습니다.

1. 두 .rc 파일이 모두 열리면 두 파일을 동시에 볼 수 있도록 창을 바둑판식으로 배열합니다.

   - **창을** 메뉴 선택 **새 가로 탭 그룹** 또는 **새 세로 탭 그룹**합니다.

       \- 또는 -

   - .Rc 파일 중 하나를 마우스 오른쪽 단추로 클릭 하 고 선택 **새 가로 탭 그룹** 하거나 **새 세로 탭 그룹** 바로 가기 메뉴에서.

> [!NOTE]
> 프로젝트에 .rc 파일이 아직 없는 경우 [새 리소스 스크립트 파일 만들기](../windows/how-to-create-a-resource-script-file.md)를 참조하세요.

## <a name="to-open-a-resource-script-file-in-text-format"></a>텍스트 형식의 리소스 스크립트 파일을 열려면

특정 리소스 편집기 내에서 대화 상자와 같은 리소스를 열지 않고 프로젝트의 리소스 스크립트(.rc) 파일의 내용을 보려는 경우가 있을 수 있습니다. 예를 들어 리소스 파일에서 각 대화 상자를 별도로 열지 않고 모든 대화 상자에서 문자열을 검색하려고 할 수 있습니다.

> [!NOTE]
> 프로젝트에 .rc 파일이 아직 없는 경우 [새 리소스 스크립트 파일 만들기](../windows/how-to-create-a-resource-script-file.md)를 참조하세요.

텍스트 형식으로 포함 된 모든 리소스 보기 및 텍스트 편집기를 지 원하는 전역 작업을 완료 하려면 리소스 파일을 쉽게 열 수 있습니다.

> [!NOTE]
> 리소스 편집기에서.rc 직접 읽지 않습니다 또는 `resource.h` 파일입니다. 리소스 컴파일러는 리소스 편집기에서 사용되는 이러한 파일을 .aps 파일로 컴파일합니다. 이 파일은 컴파일 단계이며 기호화된 데이터만 저장합니다. 일반적인 컴파일 프로세스에서처럼 기호화되지 않은 정보(예: 주석)는 컴파일 프로세스 중에 삭제됩니다. .aps 파일이 .rc 파일과 동기화되지 않을 때마다 .rc 파일이 다시 생성됩니다. 예를 들어 저장하면 리소스 편집기에서 .rc 파일 및 resource.h 파일을 덮어씁니다. 리소스 자체의 모든 변경 내용은 .rc 파일에 통합된 상태로 유지되지만 주석은 .rc 파일을 덮어쓰면 항상 손실됩니다. 주석을 유지 하는 방법에 대 한 자세한 내용은 [컴파일 타임에 리소스 포함](../windows/how-to-include-resources-at-compile-time.md)합니다.

### <a name="to-open-a-resource-script-file-as-text"></a>리소스 스크립트 파일을 텍스트로 열려면

1. **파일** 메뉴 **열려**를 선택한 **파일**합니다.

1. 에 **열려 있는 파일** 대화 상자, 텍스트 형식으로 보려는 리소스 스크립트 파일로 이동 합니다.

1. 파일을 선택한 다음에 드롭다운 화살표를 선택 합니다 **열고** 단추 (단추 오른쪽에 있음).

1. 선택할 **연결 프로그램** 드롭 다운 메뉴에서.

1. 에 **연결 프로그램** 대화 상자에서 **소스 코드 (텍스트) 편집기**합니다.

1. **형식으로 열기** 드롭 다운 목록에서 **텍스트**합니다.

   리소스에서 열립니다는 **소스 코드** 편집기입니다.

\- 또는 -

1. **솔루션 탐색기**,.rc 파일을 마우스 오른쪽 단추로 클릭 합니다.

1. 바로 가기 메뉴에서 선택 **로 열기...** 을 선택한 후 **소스 코드 (텍스트) 편집기**합니다.

## <a name="to-add-mfc-support-to-resource-script-files"></a>리소스 스크립트 파일에 MFC 지원을 추가 하려면

Windows를 사용 하 여 MFC 응용 프로그램을 빌드할 때 일반적으로 [MFC 응용 프로그램 마법사](../mfc/reference/mfc-application-wizard.md), Microsoft Foundation의 핵심 기능을 포함 하는 기본 파일 (리소스 스크립트 (.rc) 파일 포함) 집합을 생성 하는 마법사 클래스 (MFC)입니다. 그러나 MFC를 기반으로 하지 않는 Windows 응용 프로그램용.rc 파일을 편집 하는 경우 MFC 프레임 워크에 관련 된 다음 기능 사용할 수 없습니다.

- MFC 코드 마법사

- 메뉴 프롬프트 문자열

- 콤보 상자 컨트롤에 대한 내용 나열

- ActiveX 컨트롤 호스팅

그러나 없는 기존.rc 파일에 MFC 지원을 추가할 수 있습니다.

> [!NOTE]
> 이러한 단계에는 MFC 필요합니다.

### <a name="to-add-mfc-support-to-rc-files"></a>.rc 파일에 MFC 지원을 추가하려면

1. 리소스 스크립트 파일을 엽니다.

1. [리소스 뷰](../windows/resource-view-window.md), 리소스 폴더 (예: MFC.rc)를 강조 표시 합니다.

1. 에 [속성 창](/visualstudio/ide/reference/properties-window)로 설정 합니다 **MFC Mode** 속성을 **True**.

   > [!NOTE]
   > 이 플래그를 설정하는 것 외에도 .rc 파일은 MFC 프로젝트의 일부여야 합니다. 예를 들어, 설정 하는 것 **MFC Mode** 하 **True** Win32에서.rc 파일에서 프로젝트를 제공 하지 않습니다 MFC 기능입니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고자료

[리소스 파일](../windows/resource-files-visual-studio.md)<br/>
[리소스 편집기](../windows/resource-editors.md)