---
title: 연결 메뉴 명령 (c + +)
ms.date: 11/04/2016
helpviewer_keywords:
- keyboard shortcuts [C++], menu association
- commands [C++], associating menu commands with accelerator keys
- menu commands [C++], associating with keyboard shortcuts
- status bars [C++], associating menu items
- menus [C++], status bar text
- access keys [C++], checking
- menus [C++], shortcut keys
- keyboard shortcuts [C++], command assignments
- access keys [C++], assigning
- mnemonics [C++], adding to menus
- keyboard shortcuts [C++], uniqueness checking
- mnemonics [C++], uniqueness checking
- Check Mnemonics command
ms.assetid: ad2de43f-b20a-4c9f-bda8-0420179da48c
ms.openlocfilehash: f72fe5de3ef29b9575ef1a3138d4d114d7470fee
ms.sourcegitcommit: e98671a4f741b69d6277da02e6b4c9b1fd3c0ae5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55703040"
---
# <a name="associating-menu-commands-c"></a>연결 메뉴 명령 (c + +)

메뉴 명령과 키보드 조합에서 동일한 프로그램 명령을 종종 실행하도록 하려고 합니다. 사용 하 여 동일한 명령을 실행 합니다 **메뉴** 메뉴 명령 및 응용 프로그램의 액셀러레이터 키 테이블의 항목에 동일한 리소스 식별자를 할당 하는 편집기입니다. 그러고 나서 메뉴 명령의 [캡션](../windows/menu-command-properties.md) 을 편집하여 액셀러레이터 키의 이름을 표시합니다.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대한 내용은 [데스크톱 앱에 대한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)를 참조하세요. 관리되는 앱의 전역화 및 지역화 리소스에 대한 내용은 [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index)을 참조하세요.

## <a name="to-associate-a-menu-command-with-an-accelerator-key"></a>메뉴 명령을 액셀러레이터 키와 연결하려면

1. **메뉴** 편집기에서 원하는 메뉴 명령을 선택합니다.

1. [속성 창](/visualstudio/ide/reference/properties-window)에서 액셀러레이터 키 이름을 **캡션** 속성에 추가합니다.

   - 모든 메뉴의 액셀러레이터 키가 왼쪽으로 맞춰 표시되도록 메뉴 캡션 뒤에 탭의 이스케이프 시퀀스(\t)를 입력합니다.

   - 보조 키의 이름을 입력 합니다 (**Ctrl**를 **Alt**, 또는 **Shift**) 뒤에 더하기 기호 (**+**) 및 이름, 문자 또는 추가 키의 기호입니다.

       예를 들어 할당할 **Ctrl**+**O** 에 **열기** 명령을 **파일** 메뉴에서 메뉴 명령의 수정 **캡션** 다음 텍스트와 표시 되도록 합니다.

        ```
        &Open...\tCtrl+O
        ```

       메뉴 명령에는 **메뉴** 편집기 입력 한 대로 새 캡션이 반영 하도록 업데이트 됩니다.

1. [액셀러레이터](../windows/adding-an-entry-to-an-accelerator-table.md) 편집기에서 **액셀러레이터 테이블 항목을 만들고** 메뉴 명령과 같은 식별자를 할당합니다. 기억하기 쉬운 키 조합을 사용합니다.

## <a name="to-associate-a-menu-command-with-a-status-bar-text-string-in-mfc-applications"></a>메뉴 명령과 상태 표시줄 MFC 응용 프로그램에서 텍스트 문자열을 사용 하 여 연결 하려면

MFC 응용 프로그램은 각 사용자가 선택할 수 있는 메뉴 명령에 대 한 설명 텍스트를 표시할 수 있습니다. 사용 하 여 각 메뉴 명령 텍스트 문자열을 할당 하 여 설명 텍스트를 표시 합니다 **프롬프트** 속성에는 **속성** 창. 명령과 동일한 ID를 가진 문자열이 [문자열 테이블](../windows/string-editor.md) 에 있는 경우 MFC 애플리케이션은 사용자가 메뉴 항목 위로 마우스를 가져갈 때 실행 중인 애플리케이션의 상태 표시줄에 이 문자열 리소스를 자동으로 표시합니다.

1. **메뉴** 편집기에서 메뉴 명령을 선택합니다.

1. [속성 창](/visualstudio/ide/reference/properties-window)의 **프롬프트** 상자에 연결된 상태 표시줄 텍스트를 입력합니다.

> [!NOTE]
> 이 일련의 단계에는 MFC에 필요합니다.

## <a name="to-assign-an-access-shortcut-key-to-a-menu-command"></a>액세스(바로 가기) 키를 메뉴 명령에 할당하려면

C + + 프로젝트에서 메뉴 및 메뉴 명령에 액세스 키 (사용자가 키보드를 사용 하 여 메뉴를 선택할 수 있도록 니모닉)를 할당할 수 있습니다.

앰퍼샌드를 입력 (`&`) 문자 앞에 메뉴 이름이 나 명령 이름 문자를 해당 액세스 키로 지정 합니다. 예를 들어 "& 파일" 집합 **Alt**+**F** 에 대 한 바로 가기 키로는 **파일** Microsoft Windows 용으로 작성 된 응용 프로그램의 메뉴.

   메뉴 항목은 문자의 하나에 바로 가기 키가 할당되는 시각적 표시를 제공합니다. 앰퍼샌드 뒤의 문자에는 밑줄이 표시됩니다(운영 체제에 따라).

   > [!NOTE]
   > 메뉴를 마우스 오른쪽 단추로 클릭하고 바로 가기 메뉴에서 **니모닉 확인** 을 선택하여 메뉴의 모든 액세스 키가 고유한지 확인합니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고 항목

[메뉴 편집기](../windows/menu-editor.md)<br/>
[메뉴에 명령 추가](../windows/adding-commands-to-a-menu.md)<br/>
[문자열 (ATL/MFC)](../atl-mfc-shared/strings-atl-mfc.md)<br/>
