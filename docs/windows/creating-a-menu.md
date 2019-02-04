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
ms.assetid: 66f94448-9b97-4b73-bf97-10d4bf87cc65
ms.openlocfilehash: 438480032f1fe9208e406b4ee499267e42148a48
ms.sourcegitcommit: e98671a4f741b69d6277da02e6b4c9b1fd3c0ae5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55702806"
---
# <a name="creating-a-menu-c"></a>메뉴 (c + +) 만들기

> [!NOTE]
> 합니다 **리소스 창** 를 Express 버전에서는 사용할 수 없습니다.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대한 내용은 [데스크톱 앱에 대한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)를 참조하세요. 관리되는 앱의 전역화 및 지역화 리소스에 대한 내용은 [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index)을 참조하세요.

## <a name="to-create-a-standard-menu"></a>표준 메뉴를 만들려면

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

## <a name="to-insert-a-new-menu-between-existing-menus"></a>기존 메뉴 사이에 새 메뉴를 삽입하려면

기존 메뉴 이름 및 키를 눌러 선택 합니다 **삽입** 키입니다. 합니다 **새 항목** 상자 선택한 항목 앞에 삽입 됩니다.

   \- 또는 -

메뉴 모음에서 마우스 오른쪽 단추로 클릭 하 고 선택 **새로 삽입** 바로 가기 메뉴에서.

## <a name="to-add-commands-to-a-menu"></a>메뉴에 명령을 추가하려면

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

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고 항목

[메뉴 편집기](../windows/menu-editor.md)