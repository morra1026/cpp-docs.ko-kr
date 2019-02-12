---
title: '방법: 리소스 (c + +) 만들기'
ms.date: 11/04/2016
f1_keywords:
- vc.editors.resource
- vc.resvw.add.MFC
- vs.resourceview.F1
- vc.editors.insertresource
- vc.editors.newcustomresource
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
- toolbars [C++], resources
- resource toolbars
- resources [C++], creating
- Resource View window
- resources [C++], adding
- Add Resource dialog box [C++]
- Custom Resource Type dialog box [C++]
- language-specific template files [C++]
- resource templates
- rct files [C++]
- templates, resource templates
- resources [C++], templates
- .rct files [C++]
ms.assetid: 82be732a-cdcd-4a58-8de7-976d1418f86b
ms.openlocfilehash: 5a0bc6370d0973d63eb16ac992251531aa2e5193
ms.sourcegitcommit: f4be868c0d1d78e550fba105d4d3c993743a1f4b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56152393"
---
# <a name="how-to-create-resources-c"></a>방법: 리소스 (c + +) 만들기

> [!NOTE]
> 합니다 **리소스 편집기** 하거나 **리소스 뷰** Express 버전에서는 사용할 수 없습니다.
>
> 이 정보는 Windows 데스크톱 응용 프로그램 또는 유니버설 Windows 플랫폼 앱에서 리소스에 적용 되지 않습니다. .NET 언어의 프로젝트는 리소스 스크립트 파일을 사용 하지 마세요. 관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요. [리소스 파일](../windows/resource-files-visual-studio.md)하십시오 [앱 리소스 및 리소스 관리 시스템](/windows/uwp/app-resources/), 및 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에서 합니다 *.NET Framework Developer's Guide*합니다.

## <a name="create-a-resource-script"></a>리소스 스크립트 만들기

만들고 프로젝트에 새 리소스를 추가 하기 전에 먼저 리소스 스크립트 (.rc 파일)을 만들어야 합니다.

> [!NOTE]
> Visual Studio IDE에 로드된 기존 프로젝트에만 리소스 스크립트(.rc 파일)를 추가할 수 있습니다. 독립 실행형 리소스 스크립트 (외부 프로젝트를) 만들 수 없습니다. 리소스 템플릿 (.rct 파일)는 언제 든 지 만들 수 있습니다.

### <a name="to-create-a-resource-script"></a>리소스 스크립트를 만들려면

1. 기존 프로젝트 폴더에 포커스를 둡니다 **솔루션 탐색기**, 예를 들어 *MyProject*합니다.

   > [!NOTE]
   > 프로젝트 폴더의 솔루션 폴더와 혼동 하지 마세요 **솔루션 탐색기**합니다. 에 포커스를 둔 경우는 **솔루션** 폴더, 선택 항목은 **새 항목 추가** 대화 상자는 다를 수 있습니다.

1. **프로젝트** 메뉴에서 **새 항목 추가**를 선택합니다.

1. 에 **새 항목 추가** 대화 상자를 선택 합니다 **Visual c + +** 폴더를 선택 합니다. **리소스 파일 (.rc)** 오른쪽 창에서.

1. 리소스 스크립트에 대 한 이름을 제공 합니다 **이름** 텍스트 상자를 선택한 다음 선택 **열려**합니다.

### <a name="to-open-a-resource-script"></a>리소스 스크립트를 열려면

프로젝트를 열지 않고도 리소스 스크립트에서 리소스를 볼 수 있습니다. 스크립트 파일에서 열리지 않고 문서 창에 열립니다는 **리소스 뷰** 창 (마찬가지로 파일을 프로젝트 내에서 열려 있을 때).

> [!NOTE]
> 일부 명령을 파일에 열린된 독립 실행형 (외부에서 프로젝트를) 상태일 때에 사용할 수 있습니다. 독립 실행형 파일을 열고 프로젝트를 먼저 로드 하지 않고 열기 의미 합니다.
>
> 예를 들어, 다른 형식으로 또는 다른 파일 이름으로 파일을 저장 하려면 (으로 **다른 이름으로 저장** 명령이 프로젝트 내부에서 파일에 대 한 제공 되지 않습니다). 처음 사용 하 여 프로젝트를 열면 **파일** > **엽니다** > **프로젝트**, 이러한 명령을 사용할 수 없습니다.

프로젝트 외부의 리소스 스크립트를 열려면:

1. **파일** 메뉴에서 **열려**를 선택한 **파일**합니다.

1. 에 **열린 파일** 대화 상자에서 리소스 스크립트 파일로 이동한 후 파일을 강조 표시 하 고 선택 **열기**합니다.

프로젝트 외부에서 여러 리소스 스크립트를 열려면:

1. 두 리소스 파일을 모두 독립 실행형으로 엽니다. 예를 들어 열 *Source1.rc* 하 고 *Source2.rc*합니다.

1. **파일** 메뉴 선택 **열려**을 선택한 후 **파일**합니다.

1. 에 **파일 열기** 대화 상자에서 열려는 첫 리소스 스크립트 파일로 이동 (*Source1.rc*) 파일을 강조 표시 하 고 선택 **엽니다**합니다.

1. 두 번째.rc 파일을 열고 이전 단계를 반복 (*Source2.rc*).

   .rc 파일이 이제 개별 문서 창으로 열려 있습니다.

1. 두.rc 파일에서 열린 경우 합니다 **창을** 메뉴 (또는 마우스 오른쪽 단추로 클릭 한.rc 파일)을 선택 **새 가로 탭 그룹** 또는 **새 세로 탭 그룹**합니다.

   Windows는 동시에 볼 수 있도록 이제 바둑판식으로 배열 됩니다.

특정 리소스 편집기 내에서 대화 상자와 같은 리소스를 열지 않고 프로젝트의 리소스 스크립트(.rc) 파일의 내용을 보려는 경우가 있을 수 있습니다. 예를 들어 리소스 파일에서 각 대화 상자를 별도로 열지 않고 모든 대화 상자에서 문자열을 검색하려고 할 수 있습니다.

텍스트 형식으로 포함 된 모든 리소스 보기 및 텍스트 편집기를 지 원하는 전역 작업을 완료 하려면 리소스 파일을 쉽게 열 수 있습니다.

> [!NOTE]
> 리소스 편집기에서.rc 직접 읽지 않습니다 또는 `resource.h` 파일입니다. 리소스 컴파일러는 리소스 편집기에서 사용되는 이러한 파일을 .aps 파일로 컴파일합니다. 이 파일은 컴파일 단계이며 기호화된 데이터만 저장합니다. 일반적인 컴파일 프로세스에서처럼 기호화되지 않은 정보(예: 주석)는 컴파일 프로세스 중에 삭제됩니다. .Rc 파일을.aps 파일이.rc 파일과 동기화 gets, 때마다 다시 생성 됩니다 (예를 들어 저장 하면 리소스 편집기에서 파일을 덮어씁니다.rc 및 `resource.h` 파일). 리소스 자체는 변경 내용을 통합 된.rc 파일에 남지만.rc 파일을 덮어쓸지 면 주석 손실 됩니다. 주석을 유지 하는 방법에 대 한 자세한 내용은 [컴파일 타임에 리소스 포함](../windows/how-to-include-resources-at-compile-time.md)합니다.

텍스트 형식의 리소스 스크립트 파일을 열려면:

1. **파일** 메뉴 선택 **열기**를 선택한 **파일**합니다.

1. 에 **열려 있는 파일** 대화 상자, 텍스트 형식으로 보려는 리소스 스크립트 파일로 이동 합니다.

1. 파일을 선택한 다음에 드롭다운 화살표를 선택 합니다 **열기** (단추의 오른쪽)에 단추입니다.

1. 선택할 **연결 프로그램** 드롭 다운 메뉴에서.

1. 에 **연결 프로그램** 대화 상자에서 **소스 코드 (텍스트) 편집기**합니다.

1. **형식으로 열기** 드롭 다운 목록에서 **텍스트**합니다.

   리소스에서 열립니다는 **소스 코드** 편집기입니다.

> [!TIP]
> 바로 가기는의.rc 파일을 마우스 오른쪽 단추로 클릭 **솔루션 탐색기**, 선택 **로 열기...**  선택한 **소스 코드 (텍스트) 편집기**합니다.

### <a name="to-add-mfc-support"></a>MFC 지원을 추가 하려면

일반적으로 Windows를 사용 하 여 Microsoft Foundation 클래스 (MFC) 응용 프로그램을 빌드할 경우 합니다 [MFC 응용 프로그램 마법사](../mfc/reference/mfc-application-wizard.md), 마법사의 핵심 기능을 포함 하는 파일 (리소스 스크립트 (.rc) 파일 포함)의 기본 집합을 생성 합니다 MFC 합니다. 그러나 MFC 기반 하지 않는 Windows 응용 프로그램용.rc 파일을 편집할 때 다음 MFC 기능이 사용할 수 없습니다.

MFC에 관련 된 일부 기능에는 MFC 코드 마법사, 메뉴 프롬프트 문자열, 콤보 상자 컨트롤 및 ActiveX 컨트롤 호스팅에 대 한 내용 포함 됩니다.

리소스 스크립트 파일에 MFC 지원 추가:

1. 리소스 스크립트 파일을 엽니다.

1. **리소스 뷰**, 리소스 폴더 (예를 들어 *: MFC.rc*).

1. 에 [속성 창](/visualstudio/ide/reference/properties-window)로 설정 합니다 **MFC Mode** 속성을 **True**.

   > [!NOTE]
   > 이 속성을 설정 하는 것 외에도.rc 파일에는 MFC 프로젝트의 일부 여야 합니다. 예를 들어, 설정 하는 것 **MFC Mode** 하 **True** 는.rc에서 Win32 프로젝트에 있는 파일을 제공 하지 않습니다 MFC 기능입니다.

## <a name="create-a-resource"></a>리소스 만들기

리소스를 새 기본 리소스 (템플릿에 기반 하지 않는) 또는 템플릿으로 패턴화 된 리소스로 만들 수 있습니다.

새 리소스를 만들면 Visual C++은 `IDD_Dialog1`과 같은 고유 이름을 할당합니다. 연결된 리소스 편집기 또는 [속성 창](/visualstudio/ide/reference/properties-window)에서 리소스에 대한 속성을 편집하여 이 리소스 ID를 사용자 지정할 수 있습니다.

> [!NOTE]
> 리소스 이름 또는 Visual Studio에서 예약 된 ID를 지정 하지 마세요. 예약 된 이름 DESIGNINFO, HWB, 되며 TEXTINCLUDE, 고 예약된 ID는 255 까지입니다.

합니다 **리소스 뷰** 프로젝트에 포함 된 리소스 파일 창에 표시 됩니다. 상위 폴더를 확장 하면 (예를 들어 *: Project1.rc*) 파일 및 각 리소스 종류를 확장 하면 해당 형식의 개별 리소스를 보여 줍니다 내에서 리소스 유형을 보여 줍니다.

> [!TIP]
> 리소스 뷰 창을 열려면 선택 **리소스 뷰** 에 **뷰** 메뉴 (사용할지 **Ctrl** + **Shift**  +  **E**).
>
> 사용 하 여 마우스 오른쪽 단추로 클릭 합니다 **리소스 뷰** 창을 도킹 하거나 창의 도킹을 해제 하려면 제목 표시줄을 두 번 클릭 또는 명령의 바로 가기 메뉴를 시작 합니다. 제목 표시줄을 마우스 오른쪽 단추로 클릭는 창의 동작을 제어할 수 있도록 하는 추가 명령을 제공 합니다. 자세한 내용은 [Windows 관리](/visualstudio/ide/customizing-window-layouts-in-visual-studio)합니다.

사용 된 **리소스 추가** 리소스는 다음 속성을 사용 하 여 c + + Windows 데스크톱 응용 프로그램 프로젝트를 추가 하려면 대화 상자:

|속성|설명|
|-|-|
|**리소스 종류**|만들려는 리소스의 종류를 지정합니다.<br/><br/>커서와 대화 상자 리소스 범주를 확장하여 추가 리소스를 표시할 수 있습니다. 이러한 리소스가 있는 Visual Studio...\Microsoft에서 \<버전\>\VC\VCResourceTemplates\\< LCID\>\mfc.rct 합니다. .Rct 파일을 추가 하는 경우이 디렉터리에 배치 또는 다른 지정 [경로가 포함](../windows/how-to-specify-include-directories-for-resources.md)합니다. 그러면 이러한 파일의 리소스가 해당 범주의 두 번째 수준에 표시됩니다. 추가할 수 있습니다.rct 파일의 수는 미리 설정 된 제한은 없습니다.<br/><br/>트리 컨트롤의 최상위 수준에 있는 리소스는 Visual Studio에서 제공하는 기본 리소스입니다.|
|**새로 만들기**|선택한 형식에 따라 리소스를 만들어 합니다 **리소스 종류** 상자 하 고 적절 한 편집기에서 리소스를 엽니다. 예를 들어 대화 상자 리소스를 만드는 경우에서 열립니다는 [대화 상자 편집기](../windows/dialog-editor.md)합니다.|
|**Import**|열립니다는 **가져오기** 대화 상자는 이동할 수 있습니다 리소스 수를 현재 프로젝트로 가져올 하려고 합니다. 비트맵, 아이콘, 커서를 가져올 수 있습니다 HTML, 사운드 (합니다. WAV) 또는 사용자 지정 리소스 파일입니다.|
|**사용자 지정**|열립니다는 **새 사용자 지정 리소스** 대화 상자 사용자 지정 리소스를 만들 수 있습니다. 사용자 지정 리소스를 바이너리 편집기에서 편집할 수 있습니다.|

사용 된 **새 사용자 지정 리소스** 다음 속성을 사용 하 여 c + + 프로젝트에서 새 사용자 지정 리소스 만들기 대화 상자:

|속성|설명|
|-|-|
|**리소스 종류**|사용자 지정 리소스 종류의 이름을 입력 하려면 텍스트 상자를 제공 합니다. Visual c + + 이름을 종료할 때 자동으로 대문자로 시작 합니다 **새 사용자 지정 리소스** 대화 상자.|

### <a name="to-create-a-new-resource"></a>새 리소스를 만들려면

다음을 사용 하 여 새 리소스를 만들 수 있습니다.

- **리소스 뷰**,.rc 파일을 선택한 다음 선택 합니다 **편집** 메뉴 선택 **리소스 추가**합니다. 에 **리소스 추가** 대화 상자, 프로젝트에 추가 하려는 리소스 유형을 선택 합니다.

   > [!TIP]
   > .rc 파일을 마우스 오른쪽 단추로 클릭 **리소스 뷰** 선택한 **리소스 추가** 바로 가기 메뉴에서.

- **솔루션 탐색기**, 프로젝트 폴더를 마우스 오른쪽 단추로 **추가**를 선택한 **리소스 추가** 바로 가기 메뉴. 에 **리소스 추가** 대화 상자, 프로젝트에 추가 하려는 리소스 유형을 선택 합니다.

   > [!NOTE]
   > 프로젝트에.rc 파일이 없는 경우이 단계에서는 하나 만듭니다. 그런 다음 이 단계를 반복하여 새.rc 파일에 특정 리소스 형식을 추가할 수 있습니다.

- [클래스 뷰](/visualstudio/ide/viewing-the-structure-of-code)클래스를 마우스 오른쪽 단추로 클릭 하 고 선택 **추가**합니다. 선택 **리소스 추가** 바로 가기 메뉴에서 프로젝트에 추가 하려는 리소스의 종류를 선택 합니다.

- 에 **프로젝트** 메뉴 선택 **리소스 추가**합니다.

## <a name="create-a-resource-template"></a>리소스 템플릿 만들기

리소스 템플릿은.rct 파일로 저장 한 사용자 지정된 리소스입니다. 리소스 템플릿 리소스를 만들기 위한 시작 지점으로 사용 됩니다. 리소스 템플릿 리소스 추가 또는 표준 컨트롤과 같은 기능을 공유 하거나 요소를 반복 하는 리소스 그룹을 개발 시간을 저장 합니다. 예를 들어 여러 대화 상자에 회사 로고 아이콘을 사용 하 여 도움말 단추를 포함 하려는 경우 새 대화 상자 템플릿을 만들고 도움말 단추 및 로고를 사용 하 여 사용자 지정 합니다.

리소스 템플릿을 사용자 지정 후 템플릿 폴더 (또는 포함 경로에 지정 된 위치)에서 변경 내용을 저장의 리소스 형식에 새 리소스 템플릿이 표시 되도록 합니다 **리소스 추가** 대화 상자. 이제 필요에 따라 새 리소스 템플릿을 만큼 사용할 수 있습니다.

> [!NOTE]
> 리소스 편집기에서 자동으로 고유한 리소스 ID를 제공합니다. 수정할 수는 [리소스 속성](../windows/changing-the-properties-of-a-resource.md) 필요에 따라 합니다.

> [!NOTE]
> 주 템플릿 디렉터리의 하위 디렉터리에 언어별 템플릿 파일을 배치 합니다. 예를 들어 영어 전용 템플릿 파일을 배치할... \\< 리소스 템플릿 디렉터리\>\1033 합니다. Visual Studio \Program Files\Microsoft Visual Studio에서에서 새 RCT 파일을 검색 \<버전\>\Program Files\Microsoft Visual Studio에서에서 \VC\VCResourceTemplates \<버전 > \VC\VCResourceTemplates\\< LCID\> (예: 1033 영어) *또는* 어느 곳에 [포함 경로](../windows/how-to-specify-include-directories-for-resources.md)합니다. 예를 들어 내 문서가 다른 위치에 RCT 파일을 저장 하려는 경우 Visual Studio RCT 파일을 찾을 수 있도록 포함 경로에이 폴더를 추가 해야 합니다.

### <a name="to-create-a-resource-template"></a>리소스 템플릿을 만들려면

1. **솔루션 탐색기**, 프로젝트를 마우스 오른쪽 단추로 클릭 합니다.

1. 바로 가기 메뉴에서 선택 **추가**, 선택한 **새 항목 추가**합니다.

1. 에 **새 항목 추가** 대화 상자의 합니다 **템플릿:** 창 **리소스 템플릿 파일 (.rct)** 합니다.

1. 이름 및 새.rct 파일의 위치를 입력 하 고 선택 **열려**합니다.

   새.rct 파일이 프로젝트에 추가 되 고 나타나는 **솔루션 탐색기** 아래의 합니다 **리소스** 폴더입니다.

1. 문서 창에서 열려는.rct 파일을 두 번 클릭 합니다. 리소스를 추가 하려면 문서 창에서 파일을 마우스 오른쪽 단추로 클릭 하 고 선택 **리소스 추가**합니다.

   이러한 리소스를 사용자 지정 하 고.rct 파일을 저장할 수 있습니다.

### <a name="to-convert-an-existing-resource-file-to-a-template"></a>기존 리소스 파일을 템플릿으로 변환 하려면

1. 독립 실행형 파일로.rc 파일을 엽니다.

1. 에 **파일** 메뉴에서 **저장 \< *filename*>으로**입니다.

1. 위치를 지정 하 고 선택 **확인**합니다.

### <a name="to-create-a-new-resource-from-a-template"></a>템플릿에서 새 리소스를 만들려면

1. 에 **리소스 뷰** 창에서.rc 파일을 마우스 오른쪽 단추로 클릭 하 고 선택 **리소스 추가** 바로 가기 메뉴에서.

1. 에 **리소스 추가** 대화 상자에서 더하기 기호를 선택 (**+**) 리소스 노드를 확장 하 고 해당 리소스에 대 한 사용 가능한 모든 템플릿을 보려면 리소스 옆에 있는 합니다.

1. 사용할 템플릿을 두 번 클릭합니다.

1. 리소스 편집기에서 추가된 리소스를 필요에 따라 수정합니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고자료

[리소스 파일](../windows/resource-files-visual-studio.md)<br/>
[리소스 편집기](../windows/resource-editors.md)<br/>
[리소스 파일 작업](../windows/working-with-resource-files.md)<br/>