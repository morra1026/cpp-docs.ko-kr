---
title: 액세스 제어 및 값 정의
ms.date: 02/15/2019
f1_keywords:
- vc.editors.dialog.combo
helpviewer_keywords:
- access keys [C++], adding
- keyboard shortcuts [C++], controls
- dialog box controls [C++], mnemonics
- access keys [C++], checking
- mnemonics [C++], checking for duplicate
- mnemonics
- mnemonics [C++], dialog box controls
- keyboard shortcuts [C++], uniqueness checking
- Check Mnemonics command
- controls [C++], access keys
- access keys [C++]
- combo boxes [C++], Data property
- controls [C++], testing values in combo boxes
- combo boxes [C++], adding values
- combo boxes [C++], previewing values
- Data property
- combo boxes [C++], testing values
ms.assetid: 60a85435-aa30-4c5c-98b6-42fb045b9eb2
ms.openlocfilehash: 20319cd08d6d1e77faef1275e63bf3ffd354356b
ms.sourcegitcommit: 24592ba0a38c7c996ffd3d55fe1024231a59ccc2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/18/2019
ms.locfileid: "56336490"
---
# <a name="defining-control-access-and-values"></a>액세스 제어 및 값 정의

## <a name="change-the-tab-order-of-controls"></a>컨트롤의 탭 순서 변경

탭 순서는 순서를 **탭** 키 대화 상자 내에서 다음 컨트롤에서 입력된 포커스를 이동 합니다. 일반적으로 탭 순서는 왼쪽에서 오른쪽, 위쪽에서 대화 상자에서 아래쪽으로 진행 됩니다. 각 컨트롤에는 **Tabstop** 컨트롤에 입력 포커스가 있는지 여부를 결정 하는 속성입니다.

### <a name="to-set-input-focus-for-a-control"></a>컨트롤에 대 한 입력된 포커스를 설정 하려면

에 [속성 창](/visualstudio/ide/reference/properties-window)를 선택 **True** 또는 **False** 에 **Tabstop** 속성입니다.

없는 컨트롤을 **Tabstop** 속성으로 설정 **True** 탭 순서의 일부가 되도록 해야 합니다. 예를 들어 탭 순서는 중요 경우 있습니다 [액세스 키 (니모닉) 정의](../windows/defining-mnemonics-access-keys.md) 캡션이 없는 컨트롤에 대 한 합니다. 관련된 컨트롤에 대 한 액세스 키를 포함 하는 정적 텍스트 바로 앞에 나와야 관련된 컨트롤 탭 순서에서입니다.

> [!NOTE]
> 겹치는 컨트롤을 포함 하는 대화 상자에서 탭 순서 변경 컨트롤이 표시 되는 방식을 변경할 수 있습니다. 탭 순서에서 나중에 제공 되는 컨트롤은 항상 탭 순서에서 앞에 겹치는 컨트롤 위에 표시 됩니다.

### <a name="to-view-the-current-tab-order-for-all-controls-in-a-dialog-box"></a>대화 상자에서 모든 컨트롤에 대 한 현재 탭 순서를 보려면

로 이동 합니다 **형식** 메뉴를 선택 **탭 순서**를 누르거나 **Ctrl** + **D**합니다.

### <a name="to-change-the-tab-order-for-all-controls-in-a-dialog-box"></a>대화 상자에서 모든 컨트롤에 대 한 탭 순서를 변경 하려면

1. 에 **형식** 메뉴에서 **탭 순서**합니다.

   각 컨트롤의 왼쪽 위 모서리에 있는 숫자로 현재 탭 순서에서 해당 위치를 보여 줍니다.

1. 원하는 순서로 각 컨트롤을 선택 하 여 탭 순서를 설정 합니다 **탭** 키에 따라 합니다.

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

## <a name="define-mnemonics-access-keys"></a>니모닉 (선택 키)를 정의 합니다.

일반적으로 키보드 사용자 입력된 포커스를 이동 한 컨트롤에서 사용 하 여 대화 상자에서 다른 합니다 **탭** 하 고 **화살표** 키입니다. 그러나 단일 키를 눌러 컨트롤을 선택할 수 있게 해 주는 액세스 키 (니모닉 또는 기억 하기 쉬운 이름)을 정의할 수 있습니다.

### <a name="to-define-an-access-key-for-a-control-with-a-visible-caption-push-buttons-check-boxes-and-radio-buttons"></a>보이는 캡션 (누름 단추, 확인란 및 라디오 단추)를 사용 하 여 컨트롤에 대 한 액세스 키를 정의 하려면

1. 대화 상자에서 컨트롤을 선택 합니다.

1. 에 [속성 창](/visualstudio/ide/reference/properties-window)를 **캡션** 속성을 앰퍼샌드를 입력 컨트롤에 대 한 새 이름을 입력 (`&`) 해당 컨트롤에 대 한 액세스 키로 사용할 문자 앞에 합니다. 예를 들어, `&Radio1`을 입력합니다.

1. **Enter** 키를 누릅니다.

   예를 들어, 액세스 키를 나타내는 표시 캡션에 나타나는으로 밑줄 **R**(adio1).

### <a name="to-define-an-access-key-for-a-control-without-a-visible-caption"></a>표시 캡션이 없는 컨트롤에 대 한 액세스 키를 정의 하려면

1. 컨트롤에 대 한 캡션을 사용 하 여 확인을 **정적 텍스트** 에서 제어 합니다 [도구 상자](/visualstudio/ide/reference/toolbox)합니다.

1. 정적 텍스트 캡션을 앰퍼샌드를 입력 합니다 (`&`) 액세스 키로 사용할 문자 앞에 있습니다.

1. 정적 텍스트 컨트롤에 탭 순서에서 레이블 컨트롤 바로 앞에 있는지 확인 합니다.

> [!NOTE]
> 모든 액세스 키 대화 상자 내에서 고유 해야 합니다. 중복 된 선택 키를 확인 하려면로 이동 합니다 **형식** 선택한 메뉴 **니모닉 확인**합니다.

## <a name="combo-box-values"></a>콤보 상자 값

있는 그대로 콤보 상자 컨트롤에 값을 추가할 수는 **대화 상자** 편집기가 열리면 합니다.

> [!TIP]
> 콤보 상자에 모든 값을 추가 하는 것이 좋습니다 *하기 전에* 에서 크기를 지정 합니다 **대화** 편집기 콤보 컨트롤에 표시 되는 텍스트를 자를 수 있습니다.

### <a name="to-enter-values-into-a-combo-box-control"></a>콤보 상자 컨트롤에 값을 입력 하려면

1. 선택 하 여 콤보 상자 컨트롤을 선택 합니다.

1. 에 [속성 창](/visualstudio/ide/reference/properties-window), 아래로 스크롤하여 합니다 **데이터** 속성.

   > [!NOTE]
   > 유형별로 그룹화 된 속성을 표시 하는 경우 **데이터** 에 표시 되는 **기타** 속성입니다.

1. 값 영역을 선택 합니다 **데이터** 세미콜론으로 구분 된 속성 및 데이터 값을 사용 하 여 형식입니다.

   > [!NOTE]
   > 공백을 사용 드롭 다운 목록에서 사전순 정렬 되지 않으므로 값 사이 공백을 넣지 마세요.

1. 키를 눌러 **Enter** 값을 추가 했으면 합니다.

콤보 상자의 드롭다운 부분 확대에 대 한 내용은 참조 하세요 [콤보 상자 및 드롭다운 목록의 크기 설정](setting-the-size-of-the-combo-box-and-its-drop-down-list.md)합니다.

> [!NOTE]
> 값이이 절차를 사용 하 여 Win32 프로젝트에 추가할 수 없습니다 (합니다 **데이터** Win32 프로젝트에 대 한 속성은 회색). Win32 프로젝트에이 기능을 추가 하는 라이브러리가 없으므로 Win32 프로젝트를 사용 하 여 콤보 상자에 값 프로그래밍 방식으로 추가 해야 합니다.

### <a name="to-test-the-appearance-of-values-in-a-combo-box"></a>콤보 상자에서 값의 모양을 테스트 하려면

값을 입력 한 후는 **데이터** 속성을 선택 합니다 **테스트** 단추를 [대화 상자 편집기 도구 모음](../windows/showing-or-hiding-the-dialog-editor-toolbar.md)합니다.

   전체 값 목록에서 아래로 스크롤하십시오. 입력할 때 한 값이 표시 합니다 **데이터** 속성에는 **속성** 창입니다. 있습니다 맞춤법 또는 대/소문자 검사 하지 않습니다.

   키를 눌러 **Esc** 돌아가려면 합니다 **대화 상자** 편집기입니다.

   이제 선택된 상태로 표시할 라디오 단추를 지정하도록 코드를 수정할 수 있습니다. 예를 들어 `m_radioBox1 = 0;` 그룹의 첫 번째 라디오 단추를 선택 합니다.
이제 선택된 상태로 표시할 라디오 단추를 지정하도록 코드를 수정할 수 있습니다. 예를 들어 `m_radioBox1 = 0;` 그룹의 첫 번째 라디오 단추를 선택 합니다.

## <a name="radio-button-values"></a>라디오 단추의 값

대화 상자에 라디오 단추를 추가 하면 처리 그룹으로 설정 하 여는 **그룹** 속성에는 **속성** 그룹의 첫 번째 단추에 대 한 창. 그러면 해당 라디오 단추의 컨트롤 ID가 [멤버 변수 추가 마법사](../ide/add-member-variable-wizard.md)에 표시됩니다. 이 마법사를 통해 라디오 단추 그룹에 대한 멤버 변수를 추가할 수 있습니다.

대화 상자에 라디오 단추 그룹 둘 이상의 할 수 있습니다. 다음 절차를 사용 하 여 각 그룹을 추가 합니다.

### <a name="to-add-a-group-of-radio-buttons-to-a-dialog-box"></a>대화 상자에 라디오 단추 그룹을 추가하려면

1. 라디오 단추 컨트롤을 선택 합니다 [도구 상자 창](/visualstudio/ide/reference/toolbox) 컨트롤을 배치할 위치 대화 상자에서 위치를 선택 합니다.

1. 필요에 따라 라디오 단추를 추가 하는 위의 단계를 반복 합니다. 그룹의 라디오 단추가 탭 순서로 연속 되어 있는지 확인 합니다.

1. [속성 창](/visualstudio/ide/reference/properties-window)에서, 탭 순서 중 **첫 번째** 라디오 단추의 *그룹* 속성을 **True**로 설정합니다.

   변경 된 **그룹** 속성을 **True** 리소스 스크립트의 대화 상자 개체에서 단추의 항목에 WS_GROUP 스타일이 추가 하 고 사용자 수에서 한 번에 둘 이상의 라디오 단추를 선택 하는 것을 방지 단추 그룹 (그룹의 다른 사용자가 한 라디오 단추를 선택 취소 된) 경우입니다.

   > [!NOTE]
   > 그룹의 첫 번째 라디오 단추만 **그룹** 속성이 **True**로 설정되어야 합니다. 단추 그룹에 포함되지 않은 추가 컨트롤이 있는 경우 **그룹 외부에 있는** 첫 번째 컨트롤의 *그룹* 속성을 **True** 로 설정합니다. 사용 하 여 그룹 외부의 첫 번째 컨트롤을 신속 하 게 식별할 수 있습니다 **Ctrl**+**D** 탭 순서를 확인 합니다.

### <a name="to-add-a-member-variable-for-the-radio-button-group"></a>라디오 단추 그룹의 멤버 변수를 추가하려면

1. 탭 순서에서 첫 번째 라디오 단추 컨트롤을 마우스 오른쪽 단추로 클릭 (기준 컨트롤이 며 합니다 **그룹** 속성으로 설정 **True**) 선택한 **변수 추가** 에서 바로 가기 메뉴입니다.

1. [멤버 변수 추가 마법사](../ide/add-member-variable-wizard.md)에서 **제어 변수** 확인란을 선택한 후 **값** 라디오 단추를 선택합니다.

1. **변수 이름** 상자에 새 멤버 변수 이름을 입력합니다.

1. **변수 형식** 목록 상자에서 **int** 를 선택하거나 *int*를 입력합니다.

   이제 선택된 상태로 표시할 라디오 단추를 지정하도록 코드를 수정할 수 있습니다. 예를 들어 `m_radioBox1 = 0;` 그룹의 첫 번째 라디오 단추를 선택 합니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고 항목

[대화 상자의 컨트롤](../windows/controls-in-dialog-boxes.md)<br/>
[컨트롤](../mfc/controls-mfc.md)