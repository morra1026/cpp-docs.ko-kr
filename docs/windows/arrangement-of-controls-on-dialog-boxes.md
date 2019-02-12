---
title: 대화 상자 (c + +)에 컨트롤 배치 | Microsoft Docs
ms.date: 11/04/2016
f1_keywords:
- vc.editors.dialog.grouping
helpviewer_keywords:
- controls [C++], positioning
- dialog box controls [C++], placement
- Dialog Editor [C++], arranging controls
- Dialog Editor [C++], guides and margins
- guides, clearing
- guides
- dialog box controls [C++], placement
- controls [C++], guides and margins
- guides, creating
- guides, moving
- margins, moving
- DLUs (dialog units)
- controls [C++], aligning
- Dialog Editor [C++], snap to guides
- guides, tick mark interval
- dialog box controls [C++], placement
- guides, aligning controls
- dialog units (DLUs)
- snap to guides (Dialog editor)
- controls [C++], sizing
- tick mark interval in Dialog editor
- controls [C++], snap to guides/grid
- guides, disabling snapping
- controls [C++], snap to guides/grid
- controls [C++], layout grid
- snap to layout grid
- grids, turning on or off
- layout grid in Dialog Editor
- grids, changing size
- grid spacing
- guides, settings
- layout grid in Dialog Editor
- controls [C++], snap to guides/grid
- Guide Settings dialog box (Dialog editor)
- controls [C++], aligning
- controls [C++], positioning
- Space Evenly command
- dialog box controls [C++], placement
- Center in Dialog command
- Arrange Buttons command
- buttons, arranging push buttons in dialog boxes
- push buttons
- member variables, adding to radio button groups
- variables, dialog box control member variables
- dialog box controls [C++], grouping radio buttons
- grouping controls
- radio buttons [C++], grouping on dialog boxes
- controls [C++], tab order
- focus, tab order
- tab controls [C++], tab order
- Tabstop property for controls
- controls [C++], focus
- dialog box controls [C++], tab order
ms.assetid: 832491cf-98af-42e5-a854-2cb135fd45c6
ms.openlocfilehash: 210fbf8e062b4dd8c469f9c40a015bbc19bc2843
ms.sourcegitcommit: f4be868c0d1d78e550fba105d4d3c993743a1f4b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56152744"
---
# <a name="arrangement-of-controls-on-dialog-boxes-c"></a>대화 상자 (c + +)에 컨트롤 배치

합니다 **대화 상자** 편집기 컨트롤을 자동으로 크기 조정 및 정렬 하는 레이아웃 도구를 제공 합니다. 대부분의 작업을 사용 합니다 [대화 상자 편집기 도구 모음](../windows/showing-or-hiding-the-dialog-editor-toolbar.md)합니다. 모든 **대화 상자 편집기** 도구 모음 명령에서 사용할 수 있습니다 합니다 **형식** 메뉴와 대부분 [바로 가기 키](../windows/accelerator-keys-for-the-dialog-editor.md)합니다.

대화 상자에 대 한 대부분의 레이아웃 명령에 하나 이상의 컨트롤을 선택 하는 경우에에 사용할 수 있습니다. 컨트롤 하나 또는 여러 개의 컨트롤을 선택할 수 있습니다 하 고 하나 이상의 컨트롤을 선택 하면 선택한 첫 번째는 기본적으로 "주요" 컨트롤입니다. 컨트롤 및 주요 컨트롤 선택에 대 한 정보를 참조 하세요 [컨트롤 선택](../windows/selecting-controls.md)합니다.

위치, 높이 및 너비 현재 컨트롤의 상태 표시줄의 오른쪽 아래 모서리에 표시 됩니다. 전체 대화 상자를 선택 하면 상태 표시줄 전체 높이 및 너비와 대화 상자의 위치를 표시 합니다.

## <a name="dialog-editor-states-guides-and-grids"></a>대화 상자 편집기 상태 (안내선과 모눈)

사용 하 여 대화 상자에 컨트롤을 정렬할 수 있습니다 합니다 **대화 상자** 세 가지 상태 중 하나로 편집기:

- 안내선과 여백 (기본 설정)

- 레이아웃 모눈을 사용 하 여

- 모든 맞춤 또는 정렬 기능 사용 안 함

합니다 [대화 상자 편집기 도구 모음](../windows/showing-or-hiding-the-dialog-editor-toolbar.md) 상태를 제어 하는 단추가 포함 되어 있습니다. 상태를 변경 하려면 해당 아이콘을 선택 합니다. 사용 하 여 상태를 변경할 수도 있습니다는 **안내선 설정** 명령 합니다 **형식** 메뉴.

합니다 **안내선 설정** 대화 상자에는 다음 속성이 있습니다.

|속성|설명|
|---|---|
|**레이아웃 안내선**|레이아웃 안내선에 대 한 설정을 표시합니다.|
|**없음**|레이아웃 도구를 숨깁니다.|
|**눈금자 및 안내선**|레이아웃 도구;를 사용 하면 추가 눈금자 눈금자의 안내선을 배치할 수 있습니다. 기본 가이드는 여백, 끌어 이동할 수 있습니다. 눈금자의 안내선을 배치를 선택 합니다. 가이드를 통해 또는 옆에 있는 컨트롤을 이동 하는 경우에 "맞춤"를 제어 합니다. 또한 컨트롤에 연결 하는 해당 되 면 지침으로 이동 됩니다. 컨트롤에는 양쪽에 대 한 가이드에 연결 된 지침을 이동 하 고 컨트롤 크기가 조정 됩니다.|
|**눈금**|레이아웃 표를 만듭니다. 새 컨트롤 표에 자동으로 정렬 됩니다.|
|**모눈 간격**|대화 상자 단위 (Dlu) 모눈 간격에 대 한 설정을 표시합니다.|
|**너비: DLUs**|Dlu의 레이아웃 모눈의 너비를 설정합니다. 가로 DLU는 4로 나눈 대화 상자 글꼴의 평균 너비입니다.|
|**Height: DLUs**|Dlu의 레이아웃 모눈의 높이 설정합니다. 세로 DLU은 평균 8로 나눈 대화 상자 글꼴 높이입니다.|

### <a name="create-and-set-guides-and-margins"></a>만들고 안내선과 여백 설정

컨트롤을 추가 컨트롤을 이동 하 든 현재 레이아웃 다시 정렬 안내선 도움이 컨트롤 대화 상자 내에서 정확 하 게 맞춥니다. 안내선 나타나고 파란색 점선 대화 상자 편집기 및 해당 화살표의 왼쪽 맨 위에 있는 눈금자를 표시 합니다 **대화 상자** 편집기.

대화 상자를 만들 때 네 가지 여백 중 제공 됩니다. 여백은 수정 된 가이드, 파란색 점선으로 표시 합니다.

|프로세스|단계|
|----------------|----------------|
|지침을 만들려면|눈금자를 내에서 지침을 만들려면 한 번 선택 합니다. (한 번의 클릭 새로 만들고 가이드; 시작을 두 번 클릭 합니다 **안내선 설정** 가이드 설정을 지정할 수 있는 대화 상자.)|
|지침을 설정 하려면|대화 상자에서이 가이드를 클릭 하 고 새 위치로 끌어다 놓습니다. (또한 화살표를 클릭 합니다 관련된 가이드를 끌어서 눈금자의.)<br/><br/>이 가이드의 좌표는 눈금자 창의 아래쪽 상태 표시줄에 표시 됩니다. 이 가이드의 정확한 위치를 표시 하려면 눈금자 화살표 위로 포인터를 이동 합니다.|
|안내선을 삭제하려면|대화 상자에서이 가이드를 끕니다.<br/><br/>\- 또는 -<br/><br/>해당 화살표 눈금자 해제를 끕니다.|
|여백을 이동 하려면|여백을 새 위치로 끕니다.<br/><br/>사라집니다 여백을 있도록 여백을 0의 위치로 이동 합니다. 가져오고 다시 여백, 0 위치는 여백 위에 포인터를 놓고 여백을 위치로 이동 합니다.|

### <a name="align-controls-on-a-guide"></a>안내선에 컨트롤 정렬

컨트롤의 크기 조정 핸들 컨트롤을 이동 하 고 이전에 가이드에 맞춰진 컨트롤이 없는 경우 가이드 컨트롤 맞춤 안내선에 맞춤 합니다. 가이드 이동 될 때 컨트롤에 모눈을 이동 합니다. 둘 이상의 가이드에 맞춰진 컨트롤 가이드 중 하나를 이동 하면 크기가 조정 됩니다.

안내선과 컨트롤의 간격을 결정 하는 눈금자의 눈금은 대화 상자 단위 (Dlu)로 정의 됩니다. DLU는 일반적으로 8 포인트 MS Shell Dlg 대화 상자 글꼴 크기를 기반으로 합니다. 가로 DLU는 4로 나눈 대화 상자 글꼴의 평균 너비입니다. 세로 DLU은 평균 8로 나눈 글꼴 높이입니다.

#### <a name="to-size-a-group-of-controls-with-guides"></a>그룹 가이드를 사용 하 여 컨트롤의 크기

1. 안내선에 컨트롤 (또는 컨트롤)의 한 쪽을 맞춥니다.

1. 컨트롤 (또는 컨트롤)의 다른 쪽에 대 한 지침을 끕니다.

   여러 컨트롤을 사용 하 여 필요한 경우에 두 번째 가이드는 각 크기입니다.

1. 컨트롤의 크기는 (또는 컨트롤) 가이드 중 하나를 이동 합니다.

#### <a name="to-change-the-intervals-of-the-tick-marks"></a>눈금 표시의 간격을 변경 하려면

1. **형식** 메뉴 선택 **안내선 설정**합니다.

1. 에 **안내선 설정** 대화 상자의 합니다 **모눈 간격** 필드 Dlu의 새 너비와 높이 지정 합니다.

### <a name="disable-guides"></a>지침 사용 안 함

안내선의 맞춤 효과 사용 하지 않도록 설정 하려면 마우스와 함께에서 특수 키를 사용할 수 있습니다. 사용 하는 **Alt** 키 선택이 가이드의 맞춤 효과 사용 하지 않도록 설정 합니다. 지침을 사용 하 여 이동 합니다 **Shift** 키 가이드를 사용 하 여 이동 모눈된 컨트롤을 방지 합니다.

#### <a name="to-disable-the-snapping-effect-of-the-guides"></a>안내선의 맞춤 효과 사용 하지 않도록 설정

누른 채 컨트롤을 끌어 합니다 **Alt** 키입니다.

#### <a name="to-move-guides-without-moving-the-snapped-controls"></a>안내선 맞춰진된 컨트롤을 이동 하지 않고 이동 하려면

이 가이드를 누른 채 끌어서 합니다 **Shift** 키입니다.

#### <a name="to-turn-off-the-guides"></a>가이드를 사용 하지 않으려면

1. **형식** 메뉴 선택 **안내선 설정**합니다.

1. 에 **안내선 설정** 대화 상자의 **레이아웃 안내선**를 선택 **None**합니다.

   > [!NOTE]
   > 눈금자를 두 번 클릭할 수도 있습니다는 **안내선 설정** 대화 상자.

\- 또는 -

에 **형식** 메뉴에서 **안내선 설정/해제**합니다.

### <a name="modify-the-layout-grid"></a>레이아웃 모눈 수정

배치 또는 대화 상자에서 컨트롤 정렬 하는 경우에 보다 정확한 위치에 대 한 레이아웃 모눈을 사용할 수 있습니다. 표에서 켜져 컨트롤 "에 맞출" 그리드의 점선은 자석 처럼 나타납니다. 이 "눈금에 맞춤" 기능을 켜고 끄는 하 고 레이아웃 표 형태 셀의 크기를 변경할 수 있습니다.

#### <a name="to-turn-the-layout-grid-on-or-off"></a>레이아웃 모눈 켜기 / 끄기를

1. **형식** 메뉴 선택 **안내선 설정**합니다.

1. 에 **안내선 설정** 대화 상자에서 선택 하거나 선택을 취소 합니다 **표** 단추입니다.

   개별 메서드는 눈금을 제어할 수 있습니다 **대화 상자** 사용 하 여 편집기 창을 **눈금 설정/해제** 단추를 [대화 상자 편집기 도구 모음](../windows/showing-or-hiding-the-dialog-editor-toolbar.md)합니다.

#### <a name="to-change-the-size-of-the-layout-grid"></a>레이아웃 모눈의 크기를 변경 하려면

1. **형식** 메뉴 선택 **안내선 설정**합니다.

1. 에 **안내선 설정** 대화 상자에서 표의 셀에 대 한 Dlu 높이 너비를 입력 합니다. 최소 높이 또는 너비는 4 개의 Dlu입니다.

## <a name="group-radio-buttons-on-a-dialog-box"></a>대화 상자에 라디오 단추 그룹화

대화 상자에 라디오 단추를 추가 하면 처리 그룹으로 설정 하 여는 **그룹** 속성에는 **속성** 그룹의 첫 번째 단추에 대 한 창. 그러면 해당 라디오 단추의 컨트롤 ID가 [멤버 변수 추가 마법사](../ide/add-member-variable-wizard.md)에 표시됩니다. 이 마법사를 통해 라디오 단추 그룹에 대한 멤버 변수를 추가할 수 있습니다.

대화 상자에 라디오 단추 그룹이 두 개 이상 표시될 수 있으며, 각 그룹은 다음 절차에 따라 추가해야 합니다.

### <a name="to-add-a-group-of-radio-buttons-to-a-dialog-box"></a>대화 상자에 라디오 단추 그룹을 추가하려면

1. 라디오 단추 컨트롤을 선택 합니다 [도구 상자 창](/visualstudio/ide/reference/toolbox) 대화 상자의 컨트롤을 배치 하려는 위치를 선택 합니다.

1. 라디오 단추를 필요한 만큼 추가하려면 1단계를 반복합니다. 그룹의 라디오 단추가 탭 순서로 연속 되는지 확인 합니다.

1. [속성 창](/visualstudio/ide/reference/properties-window)에서, 탭 순서 중 **첫 번째** 라디오 단추의 *그룹* 속성을 **True**로 설정합니다.

   **그룹** 속성을 **True** 로 변경하면 리소스 스크립트의 대화 상자 개체에서 단추의 항목에 WS_GROUP 스타일이 추가되며, 사용자가 단추 그룹에서 한 번에 하나의 라디오 단추만 선택할 수 있게 됩니다(사용자가 라디오 단추를 하나 클릭하면 그룹의 다른 단추는 선택되지 않음).

   > [!NOTE]
   > 그룹의 첫 번째 라디오 단추만 **그룹** 속성이 **True**로 설정되어야 합니다. 단추 그룹에 포함되지 않은 추가 컨트롤이 있는 경우 **그룹 외부에 있는** 첫 번째 컨트롤의 *그룹* 속성을 **True** 로 설정합니다. 키를 눌러 그룹 외부의 첫 번째 컨트롤을 신속 하 게 식별할 수 있습니다 **Ctrl**+**D** 탭 순서를 확인 합니다.

### <a name="to-add-a-member-variable-for-the-radio-button-group"></a>라디오 단추 그룹의 멤버 변수를 추가하려면

1. 탭 순서의 첫 번째 라디오 단추 컨트롤(기준 컨트롤이며 **그룹** 속성을 True로 설정한 컨트롤)을 마우스 오른쪽 단추로 클릭합니다.

1. 바로 가기 메뉴에서 **변수 추가** 를 선택합니다.

1. [멤버 변수 추가 마법사](../ide/add-member-variable-wizard.md)에서 **제어 변수** 확인란을 선택한 후 **값** 라디오 단추를 선택합니다.

1. **변수 이름** 상자에 새 멤버 변수 이름을 입력합니다.

1. 에 **변수 형식** 목록 상자에서 **int** 또는 형식 `int`합니다.

1. 이제 선택된 상태로 표시할 라디오 단추를 지정하도록 코드를 수정할 수 있습니다. 예를 들어 `m_radioBox1 = 0;` 그룹의 첫 번째 라디오 단추를 선택 합니다.

## <a name="align-groups-of-controls"></a>컨트롤 그룹 맞춤

다음 절차에서는 컨트롤을 정렬 하는 방법을 보여 줍니다.

### <a name="to-align-groups-of-controls"></a>컨트롤의 그룹에 맞게

1. [컨트롤 선택](../windows/selecting-multiple-controls.md) 정렬 해야 합니다. 기준 컨트롤을 먼저 되도록 하려는 컨트롤을 선택 해야 하거나 맞춤을 실행 하거나 명령 크기를 조정 하기 전에 주요 컨트롤 수를 설정 합니다.

   컨트롤 그룹의 최종 위치 기준 컨트롤의 위치에 따라 달라 집니다. 기준 컨트롤 선택에 대 한 자세한 내용은 참조 하세요. [기준 컨트롤 지정](../windows/specifying-the-dominant-control.md)합니다.

1. **형식** 메뉴 선택 **Align**, 맞춤 다음 방법 중 하나를 선택:

   - `Lefts`: 선택한 컨트롤을 왼쪽으로 맞춥니다.

   - `Centers`: 선택한 컨트롤의 가운데 일렬로 가로로 맞춥니다.

   - `Rights`: 선택한 컨트롤의 오른쪽 면 일렬로 정렬 합니다.

   - `Tops`: 위쪽 가장자리를 따라 선택된 된 컨트롤에 맞춥니다.

   - `Middles`: 선택한 컨트롤의 중간 일렬로 세로로 맞춥니다.

   - `Bottoms`: 아래쪽 가장자리를 따라 선택된 된 컨트롤에 맞춥니다.

### <a name="to-even-the-spacing-between-controls"></a>컨트롤 사이의 간격을 일정

합니다 **대화 상자** 편집기 선택한 가장 바깥쪽 컨트롤 간에 균등 하 게 공간 컨트롤에 있습니다.

1. 다시 정렬 하려면 컨트롤을 선택 합니다.

1. **형식** 메뉴 선택 **균등 하 게 공간**, 다음 간격 맞춤 중 하나를 선택 하 고:

   - `Across`: 컨트롤 맨 왼쪽 및 오른쪽에 있는 선택 된 컨트롤 간에 균등 하 게 공간입니다.

   - `Down`: 컨트롤 맨 위 및 맨 아래 선택 된 컨트롤 간에 균등 하 게 공간입니다.

### <a name="to-center-controls-in-a-dialog-box"></a>대화 상자에서 컨트롤 가운데

1. 컨트롤이 나 컨트롤 다시 정렬 하려면 선택 합니다.

1. **형식** 메뉴 선택 **센터에서 대화 상자**, 다음 배치 방법 중 하나를 선택 하 고:

   - `Vertical`: 컨트롤 대화 상자에서 세로 방향으로 가운데 맞춤 합니다.

   - `Horizontal`: 컨트롤 대화 상자에서 가로 방향으로 가운데 맞춤 합니다.

### <a name="to-arrange-push-buttons-along-the-right-or-bottom-of-a-dialog-box"></a>오른쪽 또는 아래쪽 대화 상자의 누름 단추 정렬 하려면

1. 하나 이상의 푸시 단추를 선택 합니다.

1. **형식** 메뉴 선택 **단추 정렬**, 다음 배치 방법 중 하나를 선택 하 고:

   - `Right`: 대화 상자의 오른쪽 가장자리를 따라 누름 단추를 배치 합니다.

   - `Bottom`: 대화 상자의 아래쪽 가장자리를 따라 누름 단추를 배치 합니다.

       누름 단추 이외의 컨트롤을 선택할 위치로 영향을 받지 않습니다.

## <a name="change-the-tab-order-of-controls"></a>컨트롤의 탭 순서 변경

탭 순서는 순서를 **탭** 키 대화 상자 내에서 다음 컨트롤에서 입력된 포커스를 이동 합니다. 일반적으로 탭 순서는 왼쪽에서 오른쪽, 위쪽에서 대화 상자에서 아래쪽으로 진행 됩니다. 각 컨트롤에는 **Tabstop** 컨트롤에 입력 포커스가 있는지 여부를 결정 하는 속성입니다.

### <a name="to-set-input-focus-for-a-control"></a>컨트롤에 대 한 입력된 포커스를 설정 하려면

에 [속성 창](/visualstudio/ide/reference/properties-window)를 선택 **True** 또는 **False** 에 **Tabstop** 속성입니다.

없는 컨트롤을 **Tabstop** 속성으로 설정 **True** 탭 순서의 일부가 되도록 해야 합니다. 예를 들어 탭 순서는 중요 경우 있습니다 [액세스 키 (니모닉) 정의](../windows/defining-mnemonics-access-keys.md) 캡션이 없는 컨트롤에 대 한 합니다. 관련된 컨트롤에 대 한 액세스 키를 포함 하는 정적 텍스트 바로 앞에 나와야 관련된 컨트롤 탭 순서에서입니다.

> [!NOTE]
> 겹치는 컨트롤을 포함 하는 대화 상자에서 탭 순서 변경 컨트롤이 표시 되는 방식을 변경할 수 있습니다. 탭 순서에서 나중에 제공 되는 컨트롤은 항상 탭 순서에서 앞에 겹치는 컨트롤 위에 표시 됩니다.

### <a name="to-view-the-current-tab-order-for-all-controls-in-a-dialog-box"></a>대화 상자에서 모든 컨트롤에 대 한 현재 탭 순서를 보려면

에 **형식** 메뉴에서 **탭 순서**합니다.

\- 또는 -

- 키를 눌러 **Ctrl** + **D**합니다.

### <a name="to-change-the-tab-order-for-all-controls-in-a-dialog-box"></a>대화 상자에서 모든 컨트롤에 대 한 탭 순서를 변경 하려면

1. 에 **형식** 메뉴에서 **탭 순서**합니다.

   각 컨트롤의 왼쪽 위 모서리에 있는 숫자로 현재 탭 순서에서 해당 위치를 보여 줍니다.

1. 원하는 순서 대로 각 컨트롤을 클릭 하 여 탭 순서를 설정 합니다 **탭** 키에 따라 합니다.

1. 키를 눌러 **Enter** 끝내려면 **탭 순서** 모드입니다.

   > [!TIP]
   > 입력 한 후 **탭 순서** 모드를 눌러도 **Esc** 또는 **Enter** 탭 순서를 변경 하는 기능을 사용 하지 않도록 설정 합니다.

### <a name="to-change-the-tab-order-for-two-or-more-controls"></a>두 개 이상 컨트롤의 탭 순서를 변경 하려면

1. **형식** 메뉴 선택 **탭 순서**합니다.

1. 순서 변경을 시작 위치를 지정 합니다. 먼저 누른 합니다 **Ctrl** 키 컨트롤을 선택 하 고 변경된 된 순서를 시작 하려는 항목을 선택 합니다.

   예를 들어, 컨트롤의 순서를 변경 하려는 경우 `7` 를 통해 `9`를 누른 **Ctrl**를 한 컨트롤을 선택 `6` 첫 번째입니다.

   > [!NOTE]
   > 특정 컨트롤 번호를 설정 하려면 `1` (탭 순서)에서 첫 번째 컨트롤을 두 번 클릭 합니다.

1. 릴리스를 **Ctrl** 키를 다음 순서에 컨트롤을 선택 합니다 **탭** 해당 지점에서 수행 하는 키입니다.

1. 키를 눌러 **Enter** 끝내려면 **탭 순서** 모드입니다.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대한 내용은 [데스크톱 앱에 대한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)를 참조하세요. 관리되는 앱의 전역화 및 지역화 리소스에 대한 내용은 [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index)을 참조하세요.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고자료

[대화 상자의 컨트롤](../windows/controls-in-dialog-boxes.md)<br/>
[컨트롤](../mfc/controls-mfc.md)