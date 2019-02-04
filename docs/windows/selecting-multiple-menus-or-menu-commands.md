---
title: 여러 메뉴 또는 메뉴 명령 (c + +)를 편집합니다.
ms.date: 11/04/2016
helpviewer_keywords:
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
ms.assetid: b6f17897-2a40-4afd-97d4-a38b7661680b
ms.openlocfilehash: 45e2c4e97dc850b4d6fb13a5526911e4bd5caec2
ms.sourcegitcommit: e98671a4f741b69d6277da02e6b4c9b1fd3c0ae5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55703222"
---
# <a name="editing-multiple-menus-or-menu-commands"></a>여러 메뉴 또는 메뉴 명령 편집

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대한 내용은 [데스크톱 앱에 대한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)를 참조하세요. 관리되는 앱의 전역화 및 지역화 리소스에 대한 내용은 [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index)을 참조하세요.

## <a name="to-select-multiple-menu-commands"></a>여러 메뉴 명령을 선택하려면

여러 메뉴 이름이 나 메뉴 명령 속성 변경 또는 삭제와 같은 대량 작업을 실행 하기를 선택할 수 있습니다.

누른 채 합니다 **Ctrl** 키, 메뉴 또는 하위 메뉴 명령을 선택 합니다.

## <a name="to-move-and-copy-menus-and-menu-commands"></a>메뉴 및 메뉴 명령 이동 및 복사 하려면

끌어서 놓기 방법을 사용하거나 바로 가기 메뉴(오른쪽 마우스 클릭 메뉴)의 명령을 사용하여 메뉴 및 메뉴 명령을 이동하거나 복사할 수 있습니다.

### <a name="to-move-or-copy-menus-or-menu-commands-using-the-drag-and-drop-method"></a>끌어서 놓기 방법을 사용하여 메뉴 또는 메뉴 명령을 이동하거나 복사하려면

1. 이동하려는 항목을 다음 위치로 끌거나 복사합니다.

   - 현재 메뉴의 새 위치.

   - 다른 메뉴. (마우스 포인터를 다른 메뉴 위로 끌어 해당 메뉴로 이동할 수 있습니다.)

1. 삽입 가이드에 원하는 위치가 표시되면 메뉴 명령을 놓습니다.

### <a name="to-move-or-copy-menus-or-menu-commands-using-shortcut-menu-commands"></a>바로 가기 메뉴 명령을 사용하여 메뉴 또는 메뉴 명령을 이동하거나 복사하려면

1. 하나 이상의 메뉴나 메뉴 명령을 마우스 오른쪽 단추로 클릭합니다.

1. 바로 가기 메뉴에서 **잘라내기** (이동) 또는 **복사**를 선택합니다.

1. 다른 메뉴 항목을 이동 하는 경우 리소스나 리소스 스크립트 파일로 [다른 창에서 열](/visualstudio/ide/customizing-window-layouts-in-visual-studio)합니다.

1. 이동하거나 복사하려는 메뉴 또는 메뉴 명령의 위치를 선택합니다.

1. 바로 가기 메뉴에서 **붙여넣기**를 선택합니다. 이동하거나 복사한 항목은 선택한 항목 앞에 배치됩니다.

   > [!NOTE]
   > 다른 메뉴 창에 있는 다른 메뉴로 끌거나 복사하고 붙여 넣을 수도 있습니다.

## <a name="to-delete-a-menu-or-menu-command"></a>메뉴 또는 메뉴 명령을 삭제하려면

1. 메뉴 이름 또는 명령을 마우스 오른쪽 단추로 클릭합니다.

1. 바로 가기 메뉴에서 **삭제** 를 선택합니다.

   > [!NOTE]
   > 마찬가지로 바로 가기 메뉴를 사용하여 복사, 잘라내기, 붙여넣기, 새로 삽입, 구분 기호 삽입, ID 편집, 팝업으로 보기, 니모닉 확인 등의 다른 작업을 수행할 수 있습니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고 항목

[메뉴 편집기](../windows/menu-editor.md)