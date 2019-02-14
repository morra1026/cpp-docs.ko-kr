---
title: 대화 상자 편집기 (c + +)
ms.date: 11/04/2016
f1_keywords:
- vc.editors.dialog.dialog
- vc.editors.dialog.F1
- vc.editors.dialog
helpviewer_keywords:
- resource editors [C++], Dialog editor
- editors, dialog boxes
- Dialog editor
- dialog boxes [C++], editing
- controls [C++], showing or hiding Dialog editor toolbar
- toolbars [C++], showing
- toolbars [C++], hiding
- Dialog Editor [C++], showing or hiding toolbar
- events [C++], viewing for controls
- Windows messages [C++], controls
- messages [C++], viewing for dialog boxes
- Dialog Editor [C++], accessing code
- code [C++], switching from Dialog Editor
- controls [C++], jumping to code
- Dialog Editor [C++], switching between controls and code
- Dialog Editor [C++], shortcut keys
ms.assetid: d94884ef-2cca-49d8-9b58-775f34848134
ms.openlocfilehash: 827a7610aa919d5349313346ac0bfa80bd0647b0
ms.sourcegitcommit: eb2b34a24e6edafb727e87b138499fa8945f981e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2019
ms.locfileid: "56264896"
---
# <a name="dialog-editor-c"></a>대화 상자 편집기 (c + +)

합니다 **대화 상자** 편집기를 만들거나 대화 상자 리소스를 편집할 수 있습니다. 대화 상자의.rc 파일에서 두 번 클릭 하 여 대화 상자 편집기를 열면 합니다 **리소스 뷰** 창 (**뷰** > **리소스 뷰**). 사실은 **리소스 뷰** 를 Express 버전에서는 사용할 수 없습니다.

새 대화 상자(또는 대화 상자 템플릿)를 만드는 첫 번째 단계 중 하나는 대화 상자에 컨트롤을 추가하는 것입니다. 에 **대화 상자** 편집기는 특정 크기, 모양 또는 맞춤에 맞게 컨트롤을 정렬할 수 있습니다 또는 대화 상자에서 작업 하기 위한 해결 방법은 이동할 수 있습니다. 또한 컨트롤을 쉽게 삭제할 수 있습니다.

대화 상자를 템플릿으로 저장하여 다시 사용할 수 있습니다. 대화 상자 디자인과 이를 구현하는 코드 편집 간을 쉽게 전환할 수도 있습니다.

대화 상자 편집기에서 단일 또는 여러 컨트롤의 속성을 편집할 수도 있습니다. 탭 순서를 변경할 수 있습니다, 컨트롤에 대 한 나타나는 순서 즉, 포커스를 **탭** 키를 누르면 또는 키보드를 사용 하 여 컨트롤을 선택할 수 있게 해 주는 액세스 키 (키 조합)을 정의할 수 있습니다. 미리 설정된 액세스 키 목록은 [대화 상자 편집기의 액셀러레이터 키](../windows/accelerator-keys-for-the-dialog-editor.md)를 참조하세요.

합니다 **대화 상자** 편집기에서는 ActiveX 컨트롤을 포함 하 여 사용자 지정 컨트롤을 사용할 수 있습니다. 또한 [폼 보기](../mfc/reference/cformview-class.md), [레코드 뷰](../data/record-views-mfc-data-access.md)또는 [대화 상자 모음](../mfc/dialog-bars.md)을 편집할 수 있습니다.

Visual Studio 2015부터 컨트롤의 이동 및 사용자가 대화 상자 크기 조정의 크기를 조정 하는 방법을 지정 하는 동적 레이아웃을 정의 하려면 대화 상자 편집기를 사용할 수 있습니다. 자세한 내용은 [Dynamic Layout](../mfc/dynamic-layout.md)을 참조하세요.

- [새 대화 상자 만들기](../windows/creating-a-new-dialog-box.md)

- [런타임에 사용자가 종료할 수 없는 대화 상자 만들기](../windows/creating-a-dialog-box-that-users-cannot-exit.md)

- [대화 상자의 컨트롤](../windows/controls-in-dialog-boxes.md)

- [대화 상자 컨트롤에 사용할 이벤트 처리기 추가](../windows/adding-event-handlers-for-dialog-box-controls.md)

- [대화 상자 테스트](../windows/testing-a-dialog-box.md)

- [대화 상자 편집기 문제 해결](../windows/troubleshooting-the-dialog-editor.md)

   > [!TIP]
   > 사용 하는 동안 합니다 **대화 상자** 편집기, 대부분의 경우 자주 사용 되는 명령의 바로 가기 메뉴를 표시 하려면 마우스 오른쪽 단추 클릭 수 있습니다.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대한 내용은 [데스크톱 앱에 대한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)를 참조하세요. 관리되는 앱의 전역화 및 지역화 리소스에 대한 내용은 [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index)을 참조하세요.

## <a name="dialog-editor-toolbar"></a>대화 상자 편집기 도구 모음

열면 합니다 **대화 상자** c + + 프로젝트, 편집기를 **대화 상자 편집기** 솔루션의 맨 위에 있는 도구 모음이 자동으로 나타납니다.

|아이콘|의미|아이콘|의미|
|----------|-------------|----------|-------------|
|![테스트 대화 상자 단추](../mfc/media/vcdialogeditortestdialog.png "vcDialogEditorTestDialog")|대화 상자 테스트|![전체 공간 단추](../mfc/media/vcdialogeditoracross.png "vcDialogEditorAcross")|옆으로|
|![왼쪽 맞춤 단추](../mfc/media/vcdialogeditoralignlefts.png "vcDialogEditorAlignLefts")|왼쪽 맞춤|![아래 공간 단추](../mfc/media/vcdialogeditordown.png "vcDialogEditorDown")|아래로|
|![오른쪽 맞춤 단추](../mfc/media/vcdialogeditoralignrights.png "vcDialogEditorAlignRights")|오른쪽 맞춤|![확인 같은 너비로 단추](../mfc/media/vcdialogeditorsamewidth.png "vcDialogEditorSameWidth")|같은 너비로|
|![위쪽 맞춤 단추](../mfc/media/vcdialogeditoraligntops.png "vcDialogEditorAlignTops")|위쪽 맞춤|![확인 같은 높이로 단추](../mfc/media/vcdialogeditormakesameheight.png "vcDialogEditorMakeSameHeight")|같은 높이로|
|![아래쪽 맞춤 단추](../mfc/media/vcdialogeditoralignbottoms.png "vcDialogEditorAlignBottoms")|아래쪽 맞춤|![확인 같은 크기로 단추](../mfc/media/vcdialogeditorsamesize.png "vcDialogEditorSameSize")|같은 크기로|
|![세로 가운데 단추](../mfc/media/vcdialogeditorvertical.png "vcDialogEditorVertical")|세로|![눈금 단추를 토글](../mfc/media/vcdialogeditortogglegrid.png "vcDialogEditorToggleGrid")|모눈 설정/해제|
|![가로 가운데 단추](../mfc/media/vcdialogeditorhorizontal.png "vcDialogEditorHorizontal")|가로|![안내선 설정/해제 단추](../mfc/media/vcdialogeditortoggleguides.png "vcDialogEditorToggleGuides")|안내선 설정/해제|

합니다 **대화 상자 편집기** 도구 모음 단추가 대화 상자에서 예를 들어 크기 및 맞춤에서 컨트롤의 레이아웃을 정렬 합니다. **대화 상자 편집기** 도구 모음 단추에 명령에 해당 합니다 **형식** 메뉴.

있는 경우는 **대화 상자** 편집기의 표시를 전환할 수 있습니다는 **대화 상자 편집기** 사용할 수 있는 도구 모음 및 창 목록에서 선택 하 여 도구 모음입니다.

- 대화 상자 편집기 도구 모음을 표시할지를 **뷰** 메뉴에서 **도구 모음**를 선택한 **대화 상자 편집기** 하위 메뉴에서.

   > [!NOTE]
   > 합니다 **대화 상자 편집기** 도구 모음에서 대화 상자 편집기 대화 상자 리소스를 열면 기본적으로 표시 됩니다; 그러나 도구 모음을 명시적으로 닫으면 해야 대화 상자 리소스를 열면 다음에 호출 됩니다.

## <a name="switch-between-dialog-box-controls-and-code"></a>대화 상자 컨트롤과 코드 사이의 스위치

MFC 응용 프로그램에서 대화 상자 컨트롤 처리기 코드로 이동할 또는 신속 하 게 만들 스텁 처리기 함수에 두 번 클릭 수 있습니다.

선택한 컨트롤을 클릭 합니다 **컨트롤 이벤트** 단추 또는 **메시지** 단추를 [속성 창](/visualstudio/ide/reference/properties-window) Windows 메시지 및 이벤트의 전체 목록을 보려면 선택한 항목에 대해 사용할 수 있습니다. 목록에서 만들기 또는 편집 처리기 함수를 선택 합니다.

- 대화 상자 편집기에서 코드를 이동할 수는 최근에 구현 된 메시지 처리 기능에 대 한 선언으로 이동 대화 상자 내에 있는 컨트롤을 두 번 클릭 합니다. (ATL 기반 대화 상자 클래스에 대해 항상 이동할 있습니다 생성자 정의 합니다.)

- 컨트롤을 선택 하 고, 컨트롤에 대 한 이벤트를 보려면 선택 합니다 **컨트롤 이벤트** 단추를 [속성 창](/visualstudio/ide/reference/properties-window)합니다.

   > [!NOTE]
   > 선택 된 **컨트롤 이벤트** 표시 되 면 합니다 *대화 상자* 에 포커스 노출 목록이 있는 모든 컨트롤의 개별 컨트롤에 대 한 이벤트를 편집 하려면 다음 확장할 수 있는 대화 상자에서.

   마우스 오른쪽 단추로 클릭 하 고 선택할 수, 단일 컨트롤을 대화 상자에 포커스가 있으면 **이벤트 처리기 추가** 바로 가기 메뉴에서. 이 처리기가 추가 되는 클래스를 지정할 수 있습니다. 자세한 내용은 [이벤트 처리기를 추가](../ide/adding-an-event-handler-visual-cpp.md)합니다.

- 선택 대화 상자를 사용 하 여 대화 상자에 대 한 메시지를 보려면 선택 합니다 **메시지** 단추를 [속성 창](/visualstudio/ide/reference/properties-window)합니다.

## <a name="accelerator-keys"></a>액셀러레이터 키

다음은 기본 액셀러레이터 키 대화 상자 편집기 명령에 대 한 합니다. 바로 가기 키를 변경 하려면 선택 **옵션** 에 **도구** 메뉴에서 선택한 **키보드** 아래를 **환경** 폴더입니다. 자세한 내용은 [바로 가기 키 식별 및 사용자 지정](/visualstudio/ide/identifying-and-customizing-keyboard-shortcuts-in-visual-studio)을 참조하세요.

> [!NOTE]
> 대화 상자에서 사용할 수 있는 옵션과 메뉴 명령의 이름 및 위치는 실제 설정이나 버전에 따라 도움말에서 설명하는 것과 다를 수 있습니다. 설정을 변경하려면 **도구** 메뉴에서 **설정 가져오기 및 내보내기** 를 선택합니다. 자세한 내용은 [Visual Studio IDE 개인 설정](/visualstudio/ide/personalizing-the-visual-studio-ide)을 참조하세요.

|명령|키|설명|
|-------------|----------|-----------------|
|Format.AlignBottoms|**Ctrl** + **Shift** + **아래쪽 화살표**|기준 컨트롤을 사용 하 여 선택한 컨트롤의 아래쪽 가장자리에 맞춥니다.|
|Format.AlignCenters|**Shift** + **F9**|기준 컨트롤을 사용 하 여 선택한 컨트롤의 세로 가운데 맞춥니다.|
|Format.AlignLefts|**Ctrl** + **Shift** + **왼쪽 화살표**|기준 컨트롤을 사용 하 여 선택한 컨트롤의 왼쪽된 가장자리에 맞춥니다.|
|Format.AlignMiddles|**F9**|기준 컨트롤을 사용 하 여 선택한 컨트롤의 가로 가운데 맞춥니다.|
|Format.AlignRights|**Ctrl** + **Shift** + **오른쪽 화살표**|기준 컨트롤을 사용 하 여 선택한 컨트롤의 오른쪽 가장자리에 맞춥니다.|
|Format.AlignTops|**Ctrl** + **Shift** + **위쪽 화살표**|기준 컨트롤을 사용 하 여 선택한 컨트롤의 위쪽 가장자리에 맞춥니다.|
|Format.ButtonBottom|**Ctrl** + **B**|위치 선택된 대화 상자의 아래쪽 가운데 단추|
|Format.ButtonRight|**Ctrl** + **R**|대화 상자의 오른쪽 위 모서리에 선택한 단추를 배치합니다.|
|Format.CenterHorizontal|**Ctrl** + **Shift** + **F9**|대화 상자 내에서 가로로 제어 센터|
|Format.CenterVertical|**Ctrl** + **F9**|센터 대화 상자에서 세로로 컨트롤|
|Format.CheckMnemonics|**Ctrl** + **M**|니모닉의 고유성을 확인 합니다|
|Format.SizeToContent|**Shift** + **F7**|선택한 컨트롤의 캡션 텍스트에 맞게 크기 조정|
|Format.SpaceAcross|**Alt** + **왼쪽 화살표**|선택한 컨트롤을 가로 간격|
|Format.SpaceDown|**Alt** + **아래쪽 화살표**|선택한 컨트롤을 세로 간격|
|Format.TabOrder|**Ctrl** + **D**|대화 상자 내에서 컨트롤의 순서를 설정합니다.|
|Format.TestDialog|**Ctrl** + **T**|모양 및 동작을 테스트 하는 대화 상자|
|Format.ToggleGuides|**Ctrl** + **G**|대화 상자 편집을 위해 없습니다 표, 지침 및 표 간에 순환|

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고자료

[리소스 편집기](../windows/resource-editors.md)<br/>
[리소스 파일](../windows/resource-files-visual-studio.md)<br/>
[방법: 리소스 만들기](../windows/how-to-create-a-resource.md)<br/>
[컨트롤](../mfc/controls-mfc.md)<br/>
[컨트롤 클래스](../mfc/control-classes.md)<br/>
[대화 상자 클래스](../mfc/dialog-box-classes.md)<br/>
[대화 상자 컨트롤 및 변수 형식](../ide/dialog-box-controls-and-variable-types.md)