---
title: 도구 모음 (아이콘에 대 한 c + + 이미지 편집기)
ms.date: 11/04/2016
f1_keywords:
- vc.editors.bitmap
- vc.editors.icon
- vc.editors.texttool
helpviewer_keywords:
- Graphics toolbar
- Image editor [C++], toolbar
- Image editor [C++], Option selector
- Properties window
- Option selector, Image editor
- toolbars [C++], showing
- toolbars [C++], hiding
- text, adding to an image
- Text Tool dialog box [C++]
- Text Tool Font dialog box [C++]
- fonts, changing on an image
- text, on images
ms.assetid: a0af4209-6273-4106-a7c1-0edecc9b5755
ms.openlocfilehash: dfbd721afd997f3151b1c20a7e0e1fb60e0c83e4
ms.sourcegitcommit: efcc8c97570ddf7631570226c700e8f6ebb6c7be
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/01/2019
ms.locfileid: "55560324"
---
# <a name="toolbar-c-image-editor-for-icons"></a>도구 모음 (아이콘에 대 한 c + + 이미지 편집기)

합니다 **이미지 편집기** 도구 모음 그리기, 그리기, 텍스트 입력, 삭제 및 뷰를 조작에 대 한 도구를 포함 합니다. 또한 각 도구를 사용 하기 위한 옵션을 선택할 수 있는 옵션 선택기를 포함 합니다. 예를 들어, 다양 한 브러시 너비, 확대 비율 및 선 스타일에서 선택할 수 있습니다.

> [!NOTE]
> 사용할 수 있는 모든 도구를 **이미지 편집기** 도구 모음에서 사용할 수 있습니다.는 **이미지** 메뉴 (아래 합니다 **도구** 명령).

![이미지 편집기 도구 모음](../mfc/media/vcimageeditortoolbar.gif "vcImageEditorToolbar") 이미지 편집기 도구 모음

사용 하 여 **이미지 편집기** 도구 모음 및 **옵션** 선택기 도구를 선택 하거나 원하는 옵션입니다.

> [!TIP]
> 도구 모음 단추 위로 커서를 올려 놓으면 도구 설명이 표시 됩니다. 이러한 팁 각 단추의 기능을 식별할 수 있습니다.

사용 하 여 합니다 **옵션** 선택기 줄 고 브러시 스트로크 너비를 지정할 수 있습니다. 에 있는 아이콘을 **옵션** 도구에 따라 선택한 선택기 단추 변경 합니다.

![그리기&#45;이미지 편집기 도구 모음의 모양 선택기](../mfc/media/vcimageeditortoolbaroptionselector.gif "vcImageEditorToolbarOptionSelector") 이미지 편집기 도구 모음 옵션 선택기

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대한 내용은 [데스크톱 앱에 대한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)를 참조하세요. 관리되는 앱의 전역화 및 지역화 리소스에 대한 내용은 [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index)을 참조하세요.

## <a name="use-the-text-tool-dialog-box"></a>텍스트 도구 대화 상자를 사용 합니다.

사용 된 **텍스트 도구** 대화 상자에 텍스트 커서, 비트맵, 아이콘 리소스를 추가 합니다.

이 대화 상자에 액세스 하려면 엽니다는 [이미지 편집기](../windows/window-panes-image-editor-for-icons.md)합니다. 선택 **도구** 에서 합니다 **이미지** 메뉴를 선택한 후는 **텍스트 도구** 명령입니다.

### <a name="font-button"></a>글꼴 단추

열립니다는 **텍스트 도구 글꼴** 대화 상자, 글꼴, 스타일 또는 커서 글꼴의 크기를 변경할 수는 있습니다. 변경 내용이 표시 되는 텍스트에 적용 된 **텍스트** 영역입니다.

이 대화 상자에 액세스 하려면 선택 합니다 **글꼴** 단추를 **텍스트 도구** 대화 상자. 사용 가능한 속성을 다음과 같습니다.

|속성|설명|
|---|---|
|**글꼴**|사용 가능한 글꼴을 나열합니다.|
|**글꼴 스타일**|사용 가능한 지정된 된 글꼴 스타일을 나열합니다.|
|**Size**|지정된 된 글꼴에 사용할 수 있는 포인트 크기를 나열합니다.|
|**샘플**|지정 된 글꼴 설정을 사용 하 여 텍스트를 표시 하는 방법을 예제를 보여 줍니다.|
|**스크립트**|지정된 된 글꼴에 대 한 사용 가능한 언어 스크립트를 나열 합니다. 다른 언어로 스크립트를 선택 하면 문자 집합에 대 한 언어 다국어 문서를 만드는 데 사용할 수는 있습니다.|

#### <a name="to-change-the-font-of-text-on-an-image"></a>이미지의 텍스트의 글꼴을 변경 하려면

다음 절차는 Windows 응용 프로그램의 아이콘에 텍스트를 추가 하 고 텍스트의 글꼴 조작 하는 방법의 예입니다.

1. C + + Windows Forms 응용 프로그램을 만듭니다. 자세한 내용은 참조 하세요 [Windows 응용 프로그램 프로젝트를 만드는](/previous-versions/visualstudio/visual-studio-2010/42wc9kk5)합니다. *app.ico* 파일은 기본적으로 프로젝트에 추가 됩니다.

1. **솔루션 탐색기**, 파일을 두 번 클릭 *app.ico*합니다. 합니다 [이미지 편집기](../windows/image-editor-for-icons.md) 열립니다.

1. **이미지** 메뉴에서 **도구** 선택한 후 **텍스트 도구**합니다. 합니다 **텍스트 도구** 대화 상자가 표시 됩니다.

1. 에 **텍스트 도구** 대화 상자에서 *c + +* 빈 텍스트 영역에 있습니다. 이 텍스트의 왼쪽된 위 모퉁이 크기를 조정할 수 상자에 나타납니다 *app.ico*를 **이미지 편집기**합니다.

1. 에 **이미지 편집기**, 크기를 조정할 수 상자 텍스트의 가독성을 높이기 위해 app.ico의 가운데로 끕니다.

1. 에 **텍스트 도구** 대화 상자를 선택 합니다 **글꼴** 단추입니다. 합니다 **텍스트 도구 글꼴** 대화 상자가 표시 됩니다.

1. 에 **텍스트 도구 글꼴** 대화 상자에서 **Times New Roman** 에 나와 있는 사용 가능한 글꼴 목록에서를 **글꼴** 목록 상자입니다.

1. 선택 **굵게** 에 나열 된 사용 가능한 글꼴 스타일 목록을 합니다 **글꼴 스타일** 목록 상자입니다.

1. 선택 **10** 지점에 나열 된 크기의 사용 가능한 목록의 합니다 **크기** 목록 상자입니다.

1. **확인** 단추를 선택합니다. 합니다 **텍스트 도구 글꼴** 대화 상자가 닫히고 새 글꼴 설정을 텍스트에 적용 됩니다.

1. 선택 합니다 **닫습니다** 단추를 **텍스트 도구** 대화 상자. 텍스트 주위의 크기 조정 가능한 상자에서 사라집니다 합니다 **이미지 편집기**합니다.

### <a name="text-area"></a>텍스트 영역

리소스의 일부로 표시 되는 텍스트를 표시 합니다. 처음에이 영역이 비어 있습니다.

> [!NOTE]
> 하는 경우 **투명 한 배경을** 텍스트만 이미지에 배치 됨을 설정 합니다. 경우 **불투명 한 배경** 으로 설정 된 경계 사각형는 [배경색](../windows/selecting-foreground-or-background-colors-image-editor-for-icons.md), 텍스트 뒤에 배치할 수 있습니다. 자세한 내용은 [선택 투명 또는 불투명 배경](../windows/choosing-a-transparent-or-opaque-background-image-editor-for-icons.md)합니다.

마우스 오른쪽 단추로 클릭 수를 **텍스트 도구** 표준 Windows 명령 목록을 포함 하는 기본 바로 가기 메뉴에 액세스 하려면 대화 상자.

## <a name="to-display-or-hide-the-image-editor-toolbar"></a>표시 하거나 이미지 편집기 도구 모음을 숨기려면

제공 되므로 다양 한 그리기 도구를 [키보드](../windows/accelerator-keys-image-editor-for-icons.md)를 숨기려면 유용한 경우가 합니다 **이미지 편집기** 도구 모음입니다.

에 **뷰** 메뉴에서 **도구 모음** 선택한 **이미지 편집기**합니다.

   > [!NOTE]
   > 현재 프로젝트에서이 도구 모음에서 요소는 경우 이미지 파일을 사용할 수 없는 나타납니다 또는 솔루션에 열려 있지 않으면 합니다 **이미지 편집기**합니다. 참조 [아이콘 또는 다른 이미지를 만드는](../windows/creating-an-icon-or-other-image-image-editor-for-icons.md), 프로젝트에 이미지 파일 추가 대 한 정보에 대 한 합니다.

## <a name="requirements"></a>요구 사항

없음

## <a name="see-also"></a>참고 항목

[색상 창](../windows/colors-window-image-editor-for-icons.md)<br/>
[그래픽 리소스 편집](../windows/editing-graphical-resources-image-editor-for-icons.md)<br/>
[액셀러레이터 키](../windows/accelerator-keys-image-editor-for-icons.md)<br/>