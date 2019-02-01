---
title: 대화 상자 편집기 상태 (안내선과 모눈) (c + +)
ms.date: 11/04/2016
helpviewer_keywords:
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
ms.assetid: dbacf9ef-e8b0-4125-a7ce-84911c482e98
ms.openlocfilehash: 52fc19d8a39680c16692177e2758fba78afc7d3a
ms.sourcegitcommit: 5270117dbecc4c49bca0cf10b927bae3c9930038
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/31/2019
ms.locfileid: "55484996"
---
# <a name="dialog-editor-states-guides-and-grids-c"></a>대화 상자 편집기 상태 (안내선과 모눈) (c + +)

사용 하 여 대화 상자에 컨트롤을 정렬할 수 있습니다 합니다 **대화 상자** 세 가지 상태 중 하나로 편집기:

- 안내선과 여백 (기본 설정)

- 레이아웃 모눈을 사용 하 여

- 모든 맞춤 또는 정렬 기능 사용 안 함

합니다 [대화 상자 편집기 도구 모음](../windows/showing-or-hiding-the-dialog-editor-toolbar.md) 상태를 제어 하는 단추가 포함 되어 있습니다. 상태를 변경 하려면 해당 아이콘을 클릭 합니다. 사용 하 여 상태를 변경할 수도 있습니다는 **안내선 설정** 명령 합니다 **형식** 메뉴.

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

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대한 내용은 [데스크톱 앱에 대한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)를 참조하세요. 관리되는 앱의 전역화 및 지역화 리소스에 대한 내용은 [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index)을 참조하세요.

## <a name="create-and-set-guides-and-margins"></a>만들고 안내선과 여백 설정

컨트롤을 추가 컨트롤을 이동 하 든 현재 레이아웃 다시 정렬 안내선 도움이 컨트롤 대화 상자 내에서 정확 하 게 맞춥니다. 안내선 나타나고 파란색 점선 대화 상자 편집기 및 해당 화살표의 왼쪽 맨 위에 있는 눈금자를 표시 합니다 **대화 상자** 편집기.

대화 상자를 만들 때 네 가지 여백 중 제공 됩니다. 여백은 수정 된 가이드, 파란색 점선으로 표시 합니다.

### <a name="to-create-a-guide"></a>지침을 만들려면

눈금자를에서 지침을 만들려면 한 번 클릭 합니다. (한 번의 클릭 새로 만들고 가이드; 시작을 두 번 클릭 합니다 **안내선 설정** 가이드 설정을 지정할 수 있는 대화 상자.)

### <a name="to-set-a-guide"></a>지침을 설정 하려면

대화 상자에서이 가이드를 클릭 하 고 새 위치로 끌어다 놓습니다. (또한 화살표를 클릭 합니다 관련된 가이드를 끌어서 눈금자의.)

이 가이드의 좌표는 눈금자 창의 아래쪽 상태 표시줄에 표시 됩니다. 이 가이드의 정확한 위치를 표시 하려면 눈금자 화살표 위로 포인터를 이동 합니다.

### <a name="to-delete-a-guide"></a>안내선을 삭제하려면

대화 상자에서이 가이드를 끕니다.

\- 또는 -

해당 화살표 눈금자 해제를 끕니다.

### <a name="to-move-margins"></a>여백을 이동 하려면

여백을 새 위치로 끕니다.

사라집니다 여백을 있도록 여백을 0의 위치로 이동 합니다. 가져오고 다시 여백, 0 위치는 여백 위에 포인터를 놓고 여백을 위치로 이동 합니다.

## <a name="align-controls-on-a-guide"></a>안내선에 컨트롤 정렬

컨트롤의 크기 조정 핸들 컨트롤을 이동 하 고 이전에 가이드에 맞춰진 컨트롤이 없는 경우 가이드 컨트롤 맞춤 안내선에 맞춤 합니다. 가이드 이동 될 때 컨트롤에 모눈을 이동 합니다. 둘 이상의 가이드에 맞춰진 컨트롤 가이드 중 하나를 이동 하면 크기가 조정 됩니다.

안내선과 컨트롤의 간격을 결정 하는 눈금자의 눈금은 대화 상자 단위 (Dlu)로 정의 됩니다. DLU는 일반적으로 8 포인트 MS Shell Dlg 대화 상자 글꼴 크기를 기반으로 합니다. 가로 DLU는 4로 나눈 대화 상자 글꼴의 평균 너비입니다. 세로 DLU은 평균 8로 나눈 글꼴 높이입니다.

### <a name="to-size-a-group-of-controls-with-guides"></a>그룹 가이드를 사용 하 여 컨트롤의 크기

1. 안내선에 컨트롤 (또는 컨트롤)의 한 쪽을 맞춥니다.

1. 컨트롤 (또는 컨트롤)의 다른 쪽에 대 한 지침을 끕니다.

   여러 컨트롤을 사용 하 여 필요한 경우에 두 번째 가이드는 각 크기입니다.

1. 컨트롤의 크기는 (또는 컨트롤) 가이드 중 하나를 이동 합니다.

### <a name="to-change-the-intervals-of-the-tick-marks"></a>눈금 표시의 간격을 변경 하려면

1. **형식** 메뉴 선택 **안내선 설정**합니다.

1. 에 **안내선 설정** 대화 상자의 합니다 **모눈 간격** 필드 Dlu의 새 너비와 높이 지정 합니다.

## <a name="disable-guides"></a>지침 사용 안 함

안내선의 맞춤 효과 사용 하지 않도록 설정 하려면 마우스와 함께에서 특수 키를 사용할 수 있습니다. 사용 하는 **Alt** 키 선택이 가이드의 맞춤 효과 사용 하지 않도록 설정 합니다. 지침을 사용 하 여 이동 합니다 **Shift** 키 가이드를 사용 하 여 이동 모눈된 컨트롤을 방지 합니다.

### <a name="to-disable-the-snapping-effect-of-the-guides"></a>안내선의 맞춤 효과 사용 하지 않도록 설정

누른 채 컨트롤을 끌어 합니다 **Alt** 키입니다.

### <a name="to-move-guides-without-moving-the-snapped-controls"></a>안내선 맞춰진된 컨트롤을 이동 하지 않고 이동 하려면

이 가이드를 누른 채 끌어서 합니다 **Shift** 키입니다.

### <a name="to-turn-off-the-guides"></a>가이드를 사용 하지 않으려면

1. **형식** 메뉴 선택 **안내선 설정**합니다.

1. 에 **안내선 설정** 대화 상자의 **레이아웃 안내선**를 선택 **None**합니다.

   > [!NOTE]
   > 눈금자를 두 번 클릭할 수도 있습니다는 **안내선 설정** 대화 상자.

\- 또는 -

에 **형식** 메뉴에서 **안내선 설정/해제**합니다.

## <a name="modify-the-layout-grid"></a>레이아웃 모눈 수정

배치 또는 대화 상자에서 컨트롤 정렬 하는 경우에 보다 정확한 위치에 대 한 레이아웃 모눈을 사용할 수 있습니다. 표에서 켜져 컨트롤 "에 맞출" 그리드의 점선은 자석 처럼 나타납니다. 이 "눈금에 맞춤" 기능을 켜고 끄는 하 고 레이아웃 표 형태 셀의 크기를 변경할 수 있습니다.

### <a name="to-turn-the-layout-grid-on-or-off"></a>레이아웃 모눈 켜기 / 끄기를

1. **형식** 메뉴 선택 **안내선 설정**합니다.

1. 에 **안내선 설정** 대화 상자에서 선택 하거나 선택을 취소 합니다 **표** 단추입니다.

   개별 메서드는 눈금을 제어할 수 있습니다 **대화 상자** 사용 하 여 편집기 창을 **눈금 설정/해제** 단추를 [대화 상자 편집기 도구 모음](../windows/showing-or-hiding-the-dialog-editor-toolbar.md)합니다.

### <a name="to-change-the-size-of-the-layout-grid"></a>레이아웃 모눈의 크기를 변경 하려면

1. **형식** 메뉴 선택 **안내선 설정**합니다.

1. 에 **안내선 설정** 대화 상자에서 표의 셀에 대 한 Dlu 높이 너비를 입력 합니다. 최소 높이 또는 너비는 4 개의 Dlu입니다. Dlu에 대 한 자세한 내용은 참조 하세요. [대화 상자에 컨트롤의 배치](../windows/arrangement-of-controls-on-dialog-boxes.md)합니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고자료

[대화 상자의 컨트롤](../windows/controls-in-dialog-boxes.md)<br/>
[컨트롤[MFC]](../mfc/controls-mfc.md)<br/>
