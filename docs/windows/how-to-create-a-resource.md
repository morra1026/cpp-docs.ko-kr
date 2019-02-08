---
title: '방법: 리소스 (c + +) 만들기'
ms.date: 11/04/2016
f1_keywords:
- vs.resourceview.F1
- vc.editors.insertresource
- vc.editors.newcustomresource
helpviewer_keywords:
- toolbars [C++], resources
- resource toolbars
- resources [C++], creating
- resources [C++], viewing
- Resource View window
- resources [C++], adding
- Add Resource dialog box [C++]
- Custom Resource Type dialog box [C++]
ms.assetid: aad44914-9145-45a3-a7d8-9de89b366716
ms.openlocfilehash: fdf158bab7894497dbcfb147eb2c6e061879be75
ms.sourcegitcommit: 63c072f5e941989636f5a2b13800b68bb7129931
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/06/2019
ms.locfileid: "55764053"
---
# <a name="how-to-create-a-resource-c"></a>방법: 리소스 (c + +) 만들기

합니다 **리소스 뷰** 프로젝트에 포함 된 리소스 파일 창에 표시 됩니다. 최상위 폴더(예: Project1.rc)를 확장하면 해당 .rc 파일 내의 리소스 종류가 표시됩니다. 각 리소스 종류를 확장하면 해당 종류의 개별 리소스가 표시됩니다.

> [!NOTE]
> 이 정보는 유니버설 Windows 플랫폼 앱에서 리소스에 적용 되지 않습니다. 참조 하는 방법에 대 한 자세한 내용은 [앱 리소스 및 리소스 관리 시스템](/windows/uwp/app-resources/)입니다.

> [!NOTE]
> Express 버전에서는 **리소스 뷰**가 지원되지 않습니다.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다.

> [!NOTE]
> 프로젝트에 .rc 파일이 아직 없는 경우 [새 리소스 스크립트 파일 만들기](../windows/how-to-create-a-resource-script-file.md)를 참조하세요.

합니다 **리소스 뷰** 창을 사용 하는 **리소스 추가** c + + Windows 데스크톱 응용 프로그램 프로젝트에 리소스를 추가 하려면 대화 상자. 이 대화 상자에 다음 속성이 있습니다.

|속성|설명|
|---|---|
|**리소스 종류**|만들려는 리소스의 종류를 지정합니다.<br/><br/>커서와 대화 상자 리소스 범주를 확장하여 추가 리소스를 표시할 수 있습니다. 이러한 리소스가 있는 Visual Studio...\Microsoft에서 `version`\VC\VCResourceTemplates\\< LCID\>\mfc.rct 합니다. .Rct 파일을 추가,이 디렉터리에 추가 해야 하거나 지정 해야 합니다는 [경로가 포함](../windows/how-to-specify-include-directories-for-resources.md) 에 있습니다. 그러면 이러한 파일의 리소스가 해당 범주의 두 번째 수준에 표시됩니다. 추가할 수 있습니다.rct 파일의 수는 미리 설정 된 제한은 없습니다.<br/><br/>트리 컨트롤의 최상위 수준에 있는 리소스는 Visual Studio에서 제공하는 기본 리소스입니다.|
|**새로 만들기**|선택한 형식에 따라 리소스를 만들어 합니다 **리소스 종류** 상자입니다. 리소스가 해당 편집기에서 열립니다. 예를 들어 대화 상자 리소스를 만드는 경우에서 열립니다는 [대화 상자 편집기](../windows/dialog-editor.md)합니다.|
|**Import**|열립니다는 **가져올** 대화 상자는 이동할 수 있습니다 리소스 수를 현재 프로젝트로 가져올 하려고 합니다. 비트맵, 아이콘, 커서, HTML 리소스 파일, 사운드(.WAV) 리소스 파일 또는 사용자 지정 리소스 파일을 가져올 수 있습니다.|
|**사용자 지정**|열립니다는 **새 사용자 지정 리소스** 대화 상자 사용자 지정 리소스를 만들 수 있습니다. 사용자 지정 리소스는 바이너리 편집기에서만 편집할 수 있습니다.|

합니다 **새 사용자 지정 리소스** 대화 상자를 사용 하면 c + + 프로젝트에서 새 사용자 지정 리소스를 만들 수 있습니다. 이 대화 상자에 다음 속성이 있습니다.

|속성|설명|
|---|---|
|**리소스 종류**|사용자 지정 리소스 형식 이름을 입력할 텍스트 상자를 제공 합니다. Visual c + + 이름을 종료할 때 자동으로 대문자로 시작 합니다 **새 사용자 지정 리소스** 대화 상자.|

새 리소스를 만들면 Visual C++은 `IDD_Dialog1`과 같은 고유 이름을 할당합니다. 연결된 리소스 편집기 또는 [속성 창](/visualstudio/ide/reference/properties-window)에서 리소스에 대한 속성을 편집하여 이 리소스 ID를 사용자 지정할 수 있습니다.

새 기본 리소스 (템플릿에 기반 하지 않는 리소스) 또는 패턴화 된 리소스로 리소스를 만들 수는 [템플릿](../windows/how-to-use-resource-templates.md)합니다.

> [!NOTE]
> 리소스 이름 또는 Visual Studio에서 예약 된 ID를 지정 하지 마십시오. 예약된 된 이름 DESIGNINFO, HWB, 되며 TEXTINCLUDE, 고 예약된 ID는 255 까지입니다.

## <a name="to-open-the-resource-view-window"></a>리소스 뷰 창을 열려면

선택 **리소스 뷰** 에 **보기** 메뉴.

   \- 또는 -

키를 눌러 **Ctrl** + **Shift** + **E**합니다.

> [!TIP]
> 마우스 오른쪽 단추로 클릭 수를 **리소스 뷰** 명령의 바로 가기 메뉴를 시작 하는 창입니다. 제목 표시줄을 두 번 클릭하여 창을 도킹하거나 도킹 해제할 수도 있습니다. 제목 표시줄을 마우스 오른쪽 단추로 클릭하면 창의 동작을 제어할 수 있는 추가 명령이 제공됩니다. 자세한 내용은 [Windows 관리](/visualstudio/ide/customizing-window-layouts-in-visual-studio)합니다.

## <a name="to-create-a-new-resource-in-resource-view"></a>리소스 뷰에서 새 리소스를 만들려면

1. .rc 파일에 포커스를 사용 하 여 **리소스 뷰**를 선택 합니다 **편집** 메뉴 선택 **리소스 추가** (에서.rc 파일을 마우스 오른쪽 단추로 클릭 **리소스 뷰** 선택한 **리소스 추가** 바로 가기 메뉴에서).

   > [!NOTE]
   > 프로젝트에 .rc 파일이 아직 없는 경우 [새 리소스 스크립트 파일 만들기](../windows/how-to-create-a-resource-script-file.md)를 참조하세요.

1. 에 **리소스 추가** 대화 상자, 프로젝트에 추가 하려는 리소스 유형을 선택 합니다.

## <a name="to-create-a-new-resource-in-solution-explorer"></a>솔루션 탐색기에서 새 리소스를 만들려면

1. **솔루션 탐색기**에서 프로젝트 폴더를 마우스 오른쪽 단추로 클릭하고 **추가**를 선택하고 바로 가기 메뉴에서 **리소스 추가** 를 클릭합니다.

   프로젝트에.rc 파일이 없는 경우이 단계에서는 하나 만듭니다. 그런 다음 이 단계를 반복하여 새.rc 파일에 특정 리소스 형식을 추가할 수 있습니다.

2. 에 **리소스 추가** 대화 상자, 프로젝트에 추가 하려는 리소스 유형을 선택 합니다.

## <a name="to-create-a-new-resource-in-class-view"></a>클래스 뷰에서 새 리소스를 만들려면

1. [클래스 뷰](/visualstudio/ide/viewing-the-structure-of-code)클래스를 마우스 오른쪽 단추로 클릭 하 고 선택 **추가**을 선택한 후 **리소스 추가** 바로 가기 메뉴에서.

2. 에 **리소스 추가** 대화 상자, 프로젝트에 추가 하려는 리소스 유형을 선택 합니다.

## <a name="to-create-a-new-resource-from-the-project-menu"></a>프로젝트 메뉴에서 새 리소스를 만들려면

**프로젝트** 메뉴에서 **리소스 추가**를 선택합니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고자료

[리소스 파일 작업](../windows/working-with-resource-files.md)<br/>
[리소스 파일](../windows/resource-files-visual-studio.md)<br/>
[리소스 편집기](../windows/resource-editors.md)<br/>
