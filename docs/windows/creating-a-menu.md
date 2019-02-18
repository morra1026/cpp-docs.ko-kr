---
title: 메뉴 (c + +) 만들기
ms.date: 11/04/2016
f1_keywords:
- vc.editors.menu
helpviewer_keywords:
- mnemonics [C++], associating menu items
- menus [C++], associating commands with mnemonic keys
- menus [C++], creating
- menus [C++], adding items
- commands [C++], adding to menus
- menu items, adding to menus
- submenus
- submenus [C++], creating
- menus [C++], creating
- context menus [C++], Menu Editor
- pop-up menus [C++], creating
- menus [C++], pop-up
- menus [C++], creating
- shortcut menus [C++], creating
- pop-up menus [C++], displaying
- pop-up menus [C++], connecting to applications
- context menus [C++], connecting to applications
- shortcut menus [C++], connecting to applications
- pop-up menus
- menu commands [C++], selecting
- menus [C++], selecting
- commands [C++], menu commands
- commands [C++], copying on menus
- menu items, moving
- commands [C++], moving on menus
- menu items, copying
- menu items, deleting
- commands [C++], deleting from menus
- menus [C++], deleting
ms.assetid: 66f94448-9b97-4b73-bf97-10d4bf87cc65
ms.openlocfilehash: da5fc355ae11ee5efb1c58be9e33bd4fb8bff02d
ms.sourcegitcommit: 470de1337035dd33682d935b4b6c6d8b1bdb0bbb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56320525"
---
# <a name="creating-menus-c"></a>메뉴 (c + +) 만들기

> [!NOTE]
> 합니다 **리소스 창** 를 Express 버전에서는 사용할 수 없습니다.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대한 내용은 [데스크톱 앱에 대한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)를 참조하세요. 관리되는 앱의 전역화 및 지역화 리소스에 대한 내용은 [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index)을 참조하세요.

## <a name="create-a-standard-menu"></a>표준 메뉴 만들기

1. **보기** 메뉴에서 **리소스 뷰** 에서 마우스 오른쪽 단추로 클릭 하 고는 **메뉴** 제목 및 선택 **리소스 추가**합니다. **메뉴**를 선택합니다.

1. 메뉴 모음에서 **새 항목** 상자(“여기에 입력”이 포함된 사각형)를 선택합니다.

   ![메뉴 편집기에서 새 항목 상자가](../windows/media/vcmenueditornewitembox.gif "vcMenuEditorNewItemBox")<br/>
   새 항목 상자

1. 예를 들어 "파일"과 같이 새 메뉴의 이름을 입력합니다.

   입력하는 텍스트는 **메뉴** 편집기와 **속성 창** 의 [캡션](/visualstudio/ide/reference/properties-window)상자에 모두 나타납니다. 한 위치에서 새 메뉴에 대한 속성을 편집할 수 있습니다.

   메뉴 모음에서 새 메뉴에 이름을 지정하면 새 항목 상자가 오른쪽으로 이동하고(다른 메뉴를 추가할 수 있도록), 메뉴 명령을 추가할 수 있도록 또 다른 새 항목 상자가 첫 번째 메뉴 아래에 열립니다.

   ![확장 된 새 항목 상자가](../windows/media/vcmenueditornewitemboxexpanded.gif "vcMenuEditorNewItemBoxExpanded")<br/>
   메뉴 이름을 입력한 후 포커스가 이동된 새 항목 상자

   > [!NOTE]
   > 메뉴 모음에서 단일 항목 메뉴를 만들려면 다음을 설정 합니다 **팝업** 속성을 **False**합니다.

## <a name="create-a-submenu"></a>하위 메뉴 만들기

1. 하위 메뉴를 만들려는 메뉴 명령을 선택 합니다.

1. 오른쪽에 표시되는 **새 항목** 상자에 새 메뉴 명령의 이름을 입력합니다. 이 새로운 명령이 하위 메뉴에서 첫 번째로 표시됩니다.

1. 하위 메뉴에 메뉴 명령을 더 추가합니다.

## <a name="to-insert-a-new-menu-between-existing-menus"></a>기존 메뉴 사이에 새 메뉴를 삽입하려면

기존 메뉴 이름 및 키를 눌러 선택 합니다 **삽입** 키입니다. 합니다 **새 항목** 상자 선택한 항목 앞에 삽입 됩니다.

   \- 또는 -

메뉴 모음에서 마우스 오른쪽 단추로 클릭 하 고 선택 **새로 삽입** 바로 가기 메뉴에서.

## <a name="add-commands-to-a-menu"></a>메뉴에 명령 추가

1. 메뉴를 만듭니다.

1. 예를 들어 메뉴 이름을 선택한 **파일**합니다.

   각 메뉴가 확장되고 명령에 대한 새 항목 상자가 표시됩니다. 예를 들어 명령을 추가할 수 있습니다 **새로 만들기**, **열려**, 및 **닫기** 하는 **파일** 메뉴.

1. 새 항목 상자에 새 메뉴 명령에 대한 이름을 입력합니다.

   > [!NOTE]
   > 입력하는 텍스트는 **메뉴** 편집기와 **속성 창** 의 [캡션](/visualstudio/ide/reference/properties-window)상자에 모두 나타납니다. 한 위치에서 새 메뉴에 대한 속성을 편집할 수 있습니다.

   > [!TIP]
   > 사용자가 메뉴 명령을 선택할 수 있도록 니모닉 키(바로 가기 키)를 정의할 수 있습니다. 앰퍼샌드를 입력 (`&`) 니모닉으로 지정 하려면 문자 앞에 있습니다. 사용자는 해당 문자를 입력하여 메뉴 명령을 선택할 수 있습니다.

1. 에 **속성** 창에서 메뉴 명령을 적용 되는 속성입니다. 자세한 내용은 참조 하세요 [메뉴 명령 속성](../windows/menu-command-properties.md)합니다.

1. 에 **프롬프트** 상자에 **속성** 창 응용 프로그램의 상태 표시줄에 표시할 프롬프트 문자열을 입력 합니다.

   이 단계에서 만든 메뉴 명령과 동일한 리소스 식별자를 사용 하 여 문자열 테이블 항목을 만듭니다.

   > [!NOTE]
   > 프롬프트 메뉴 항목에만 적용할 수는 **팝업** 속성을 **True**합니다. 예를 들어 최상위 메뉴 항목은 하위 메뉴 항목이 있는 경우 프롬프트가 적용됩니다. 용도 **프롬프트** 어떤 동작이 발생 했다는 것을 사용자가 메뉴 항목을 선택 합니다.

1. 키를 눌러 **Enter** 메뉴 명령을 완료 합니다.

   새 항목 상자를 선택하여 추가 메뉴 명령을 만들 수 있습니다.

## <a name="create-pop-up-menus"></a>팝업 메뉴 만들기

[팝업 메뉴](../mfc/menus-mfc.md) 에는 자주 사용되는 명령이 표시됩니다. 포인터 위치에 대한 상황에 맞는 메뉴일 수 있습니다. 애플리케이션에서 팝업 메뉴를 사용하려면 메뉴 자체를 빌드한 후 애플리케이션 코드에 연결해야 합니다.

메뉴 리소스를 만든 후에 응용 프로그램 코드 메뉴 리소스를 로드 하 여 사용 해야 [TrackPopupMenu](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) 를 메뉴를 표시 합니다. 사용자가 팝업 메뉴 바깥쪽을 선택 하 여 해제 된 또는 명령을 선정 되 면 해당 함수가 반환 됩니다. 사용자가 명령을 선택하는 경우 해당 명령 메시지가 핸들이 전달된 창으로 전송됩니다.

### <a name="to-create-a-pop-up-menu"></a>팝업 메뉴를 만들려면

1. 빈 제목을 사용하여[메뉴를 만듭니다](../windows/creating-a-menu.md) . **캡션**을 제공하지 마세요.

1. [새 메뉴에 메뉴 명령을 추가](../windows/adding-commands-to-a-menu.md)합니다. 빈 메뉴 제목 아래 첫 번째 메뉴 명령을 이동 (이라는 임시 캡션이 `Type Here`). **캡션** 및 기타 정보를 입력합니다.

   팝업 메뉴의 다른 모든 메뉴 명령에 대해 이 프로세스를 반복합니다.

1. 메뉴 리소스를 저장합니다.

### <a name="to-connect-a-pop-up-menu-to-your-application"></a>응용 프로그램에 팝업 메뉴를 연결하려면

1. 예를 들어 WM_CONTEXTMENU에 대 한 메시지 처리기를 추가 합니다. 자세한 내용은 [함수에 메시지 매핑](../mfc/reference/mapping-messages-to-functions.md)합니다.

1. 메시지 처리기에 다음 코드를 추가합니다.

    ```cpp
    CMenu menu;
    VERIFY(menu.LoadMenu(IDR_MENU1));
    CMenu* pPopup = menu.GetSubMenu(0);
    ASSERT(pPopup != NULL);
    pPopup->TrackPopupMenu(TPM_LEFTALIGN | TPM_RIGHTBUTTON, point.x, point.y, AfxGetMainWnd());
    ```

   > [!NOTE]
   > 합니다 [CPoint](../atl-mfc-shared/reference/cpoint-class.md) 전달 된 메시지 처리기는 화면 좌표입니다.

   > [!NOTE]
   > 응용 프로그램에 팝업 메뉴 연결 MFC에 필요 합니다.

### <a name="to-view-a-menu-resource-as-a-pop-up-menu"></a>메뉴 리소스를 팝업 메뉴로 보려면

일반적으로 작업는 **메뉴** 편집기 메뉴 리소스 메뉴 모음으로 표시 됩니다. 그러나 프로그램이 실행되는 동안 응용 프로그램의 메뉴 모음에 메뉴 리소스가 추가될 수 있습니다.

메뉴를 마우스 오른쪽 단추로 클릭 하 고 선택 **팝업으로 보기** 바로 가기 메뉴에서.

   이 옵션 보기 설정 이며 메뉴를 수정 하지 않습니다.

   > [!NOTE]
   > 메뉴 모음 보기로 다시 변경 하려면 **팝업으로 보기** 다시 (확인 표시를 제거 하며 메뉴 모음 보기를 반환 합니다).

## <a name="edit-multiple-menus-or-menu-commands"></a>여러 메뉴 또는 메뉴 명령 편집

### <a name="to-select-multiple-menu-commands"></a>여러 메뉴 명령을 선택하려면

여러 메뉴 이름이 나 메뉴 명령 속성 변경 또는 삭제와 같은 대량 작업을 실행 하기를 선택할 수 있습니다.

누른 채 합니다 **Ctrl** 키, 메뉴 또는 하위 메뉴 명령을 선택 합니다.

### <a name="to-move-and-copy-menus-and-menu-commands"></a>메뉴 및 메뉴 명령 이동 및 복사 하려면

끌어서 놓기 방법을 사용하거나 바로 가기 메뉴(오른쪽 마우스 클릭 메뉴)의 명령을 사용하여 메뉴 및 메뉴 명령을 이동하거나 복사할 수 있습니다.

#### <a name="to-move-or-copy-menus-or-menu-commands-using-the-drag-and-drop-method"></a>끌어서 놓기 방법을 사용하여 메뉴 또는 메뉴 명령을 이동하거나 복사하려면

1. 이동하려는 항목을 다음 위치로 끌거나 복사합니다.

   - 현재 메뉴의 새 위치.

   - 다른 메뉴. (마우스 포인터를 다른 메뉴 위로 끌어 해당 메뉴로 이동할 수 있습니다.)

1. 삽입 가이드에 원하는 위치가 표시되면 메뉴 명령을 놓습니다.

#### <a name="to-move-or-copy-menus-or-menu-commands-using-shortcut-menu-commands"></a>바로 가기 메뉴 명령을 사용하여 메뉴 또는 메뉴 명령을 이동하거나 복사하려면

1. 하나 이상의 메뉴나 메뉴 명령을 마우스 오른쪽 단추로 클릭합니다.

1. 바로 가기 메뉴에서 **잘라내기** (이동) 또는 **복사**를 선택합니다.

1. 다른 메뉴 항목을 이동 하는 경우 리소스나 리소스 스크립트 파일로 [다른 창에서 열](/visualstudio/ide/customizing-window-layouts-in-visual-studio)합니다.

1. 이동하거나 복사하려는 메뉴 또는 메뉴 명령의 위치를 선택합니다.

1. 바로 가기 메뉴에서 **붙여넣기**를 선택합니다. 이동하거나 복사한 항목은 선택한 항목 앞에 배치됩니다.

   > [!NOTE]
   > 다른 메뉴 창에 있는 다른 메뉴로 끌거나 복사하고 붙여 넣을 수도 있습니다.

### <a name="to-delete-a-menu-or-menu-command"></a>메뉴 또는 메뉴 명령을 삭제하려면

1. 메뉴 이름 또는 명령을 마우스 오른쪽 단추로 클릭합니다.

1. 바로 가기 메뉴에서 **삭제** 를 선택합니다.

   > [!NOTE]
   > 마찬가지로 바로 가기 메뉴를 사용하여 복사, 잘라내기, 붙여넣기, 새로 삽입, 구분 기호 삽입, ID 편집, 팝업으로 보기, 니모닉 확인 등의 다른 작업을 수행할 수 있습니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고자료

[메뉴 편집기](../windows/menu-editor.md)