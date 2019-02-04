---
title: 팝업 메뉴 (c + +) 만들기
ms.date: 11/04/2016
helpviewer_keywords:
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
ms.assetid: dff4dddf-2e8d-4c34-b755-90baae426b58
ms.openlocfilehash: cf2e3578f49cb6b4af8797052273211f699a6b4f
ms.sourcegitcommit: e98671a4f741b69d6277da02e6b4c9b1fd3c0ae5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55702832"
---
# <a name="creating-pop-up-menus-c"></a>팝업 메뉴 (c + +) 만들기

[팝업 메뉴](../mfc/menus-mfc.md) 에는 자주 사용되는 명령이 표시됩니다. 포인터 위치에 대한 상황에 맞는 메뉴일 수 있습니다. 애플리케이션에서 팝업 메뉴를 사용하려면 메뉴 자체를 빌드한 후 애플리케이션 코드에 연결해야 합니다.

메뉴 리소스를 만든 후에 응용 프로그램 코드 메뉴 리소스를 로드 하 여 사용 해야 [TrackPopupMenu](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) 를 메뉴를 표시 합니다. 사용자가 팝업 메뉴 바깥쪽을 선택 하 여 해제 된 또는 명령을 선정 되 면 해당 함수가 반환 됩니다. 사용자가 명령을 선택하는 경우 해당 명령 메시지가 핸들이 전달된 창으로 전송됩니다.

## <a name="to-create-a-pop-up-menu"></a>팝업 메뉴를 만들려면

1. 빈 제목을 사용하여[메뉴를 만듭니다](../windows/creating-a-menu.md) . **캡션**을 제공하지 마세요.

1. [새 메뉴에 메뉴 명령을 추가](../windows/adding-commands-to-a-menu.md)합니다. 빈 메뉴 제목 아래 첫 번째 메뉴 명령을 이동 (이라는 임시 캡션이 `Type Here`). **캡션** 및 기타 정보를 입력합니다.

   팝업 메뉴의 다른 모든 메뉴 명령에 대해 이 프로세스를 반복합니다.

1. 메뉴 리소스를 저장합니다.

## <a name="to-connect-a-pop-up-menu-to-your-application"></a>응용 프로그램에 팝업 메뉴를 연결하려면

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

## <a name="to-view-a-menu-resource-as-a-pop-up-menu"></a>메뉴 리소스를 팝업 메뉴로 보려면

일반적으로 작업는 **메뉴** 편집기 메뉴 리소스 메뉴 모음으로 표시 됩니다. 그러나 프로그램이 실행되는 동안 응용 프로그램의 메뉴 모음에 메뉴 리소스가 추가될 수 있습니다.

메뉴를 마우스 오른쪽 단추로 클릭 하 고 선택 **팝업으로 보기** 바로 가기 메뉴에서.

   이 옵션 보기 설정 이며 메뉴를 수정 하지 않습니다.

   > [!NOTE]
   > 메뉴 모음 보기로 다시 변경 하려면 **팝업으로 보기** 다시 (확인 표시를 제거 하며 메뉴 모음 보기를 반환 합니다).

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고 항목

[메뉴 편집기](../windows/menu-editor.md)
