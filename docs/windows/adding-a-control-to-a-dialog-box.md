---
title: 대화 상자 (c + +)에 컨트롤 추가
ms.date: 11/04/2016
f1_keywords:
- vc.editors.dialog.dialog
helpviewer_keywords:
- dialog boxes [C++], adding controls to
- Toolbox [C++], Dialog Editor tab
- controls [C++], types
- syslink controls in dialog boxes
- custom controls [C++], dialog boxes
- controls [C++], standard
- Dialog Editor [C++], creating controls
- controls [C++], adding to dialog boxes
- controls [C++], adding multiple
- dialog box controls [C++], size
- controls [C++], sizing
ms.assetid: b2a26d19-093f-49ca-93da-fef00dfbb381
ms.openlocfilehash: 92b644769bcbe2649d00ba68437bd474ee06dfcc
ms.sourcegitcommit: b488462a6e035131121e6f32d8f3b108cc798b5e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55293626"
---
# <a name="adding-a-control-to-a-dialog-box-c"></a>대화 상자 (c + +)에 컨트롤 추가

합니다 **대화 상자 편집기** 탭에 표시 됩니다는 [도구 상자 창](/visualstudio/ide/reference/toolbox) 에서 작업 하는 경우는 **대화** 편집기입니다. 새 대화 상자에 컨트롤을 추가할 컨트롤을 끌어 옵니다 합니다 **도구 상자** 만드는 대화 상자. 그런 다음 컨트롤을 주변으로 이동하거나 크기와 모양을 변경할 수 있습니다.

사용할 수 있는 표준 컨트롤을 **도구 상자** 됩니다.

- [단추 컨트롤](../mfc/reference/cbutton-class.md)

- [확인란 컨트롤](../mfc/reference/styles-used-by-mfc.md#button-styles)

- [콤보 상자 컨트롤](../mfc/reference/ccombobox-class.md)

- [편집 컨트롤](../mfc/reference/cedit-class.md)

- 그룹 상자

- [목록 상자 컨트롤](../mfc/reference/clistbox-class.md)

- [라디오 단추 컨트롤](../mfc/reference/styles-used-by-mfc.md#button-styles)

- [정적 텍스트 컨트롤](../mfc/reference/cstatic-class.md)

- [그림 컨트롤](../mfc/reference/cpictureholder-class.md)

- [Rich Edit 2.0 컨트롤](../mfc/using-cricheditctrl.md)

- [스크롤 막대 컨트롤](../mfc/reference/cscrollbar-class.md)

합니다 [Windows 공용 컨트롤](../mfc/controls-mfc.md) 에서 사용할 수 있는 합니다 **도구 상자** 응용 프로그램에 향상 된 기능을 제공 합니다. 다음과 같은 변경 내용이 해당됩니다.

- [슬라이더 컨트롤](../mfc/slider-control-styles.md)

- [스핀 컨트롤](../mfc/using-cspinbuttonctrl.md)

- [진행률 컨트롤](../mfc/styles-for-the-progress-control.md)

- [Hot Key 컨트롤](../mfc/using-a-hot-key-control.md)

- [목록 컨트롤](../mfc/list-control-and-list-view.md)

- [트리 컨트롤](../mfc/tree-control-styles.md)

- [탭 컨트롤](../mfc/tab-controls-and-property-sheets.md)

- [애니메이션 컨트롤](../mfc/using-an-animation-control.md)

- [날짜 시간 선택 컨트롤](../mfc/creating-the-date-and-time-picker-control.md)

- [Monthcalendar 컨트롤](../mfc/month-calendar-control-examples.md)

- [IP 주소 컨트롤](../mfc/reference/cipaddressctrl-class.md)

- [확장 된 콤보 상자 컨트롤](../mfc/creating-an-extended-combo-box-control.md)

- [사용자 지정 컨트롤](custom-controls-in-the-dialog-editor.md)

선택 하 여 대화 상자에 사용자 지정 컨트롤을 추가할 수 있습니다는 **사용자 지정 컨트롤** 아이콘에는 **도구 상자** 끌어서 놓아 대화 상자. 추가 하는 **Syslink** 컨트롤, 사용자 지정 컨트롤을 추가한 다음 컨트롤의 변경 **클래스** 속성을 **Syslink**합니다. 이렇게 하면 새로 고치고 표시 속성을 **Syslink** 속성을 제어 합니다. MFC 래퍼 클래스에 대 한 자세한 내용은 [CLinkCtrl](../mfc/reference/clinkctrl-class.md)합니다.

수도 있습니다 [대화 상자에 ActiveX 컨트롤을 추가할](../windows/viewing-and-adding-activex-controls-to-a-dialog-box.md)합니다.

사용자 지정할 수도 있습니다는 **도구 상자** 창을 쉽게 사용할 수 있도록 합니다. 자세한 내용은 [도구 상자 사용](/visualstudio/ide/using-the-toolbox)을 참조하세요.

사용 하 여 대 한 자세한 내용은 합니다 **RichEdit 1.0** 내용은 MFC를 사용 하 여 제어 [MFC에 RichEdit 1.0 컨트롤 사용](../windows/using-the-richedit-1-0-control-with-mfc.md)

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대한 내용은 [데스크톱 앱에 대한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)를 참조하세요. 관리되는 앱의 전역화 및 지역화 리소스에 대한 내용은 [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index)을 참조하세요.

## <a name="to-add-a-control-to-a-dialog-box"></a>대화 상자에 컨트롤을 추가하려면

1. 대화 상자 탭 창이 편집기 프레임에서 현재 문서인지 확인합니다. 대화 상자에서 현재 문서에 없는 경우 볼 수 없습니다는 **대화 상자 편집기 탭** 에 **도구 상자**합니다.

1. 에 **대화 상자 편집기** 탭을 [도구 상자 창](/visualstudio/ide/reference/toolbox), 한 다음 원하는 컨트롤을 선택:

   - 대화 상자 컨트롤을 배치 하려는 위치를 선택 합니다. 컨트롤을 선택한 위치 표시 됩니다.

       \- 또는 -

   - 끌어서 놓기 컨트롤을 **도구 상자** 대화 상자에서 위치를 창입니다.

       \- 또는 -

   - 컨트롤을 두 번 클릭 합니다 **도구 상자** 창 (대화 상자에 표시)을 원하는 위치로 컨트롤 위치를 변경 합니다.

## <a name="to-add-multiple-controls"></a>여러 컨트롤을 추가 하려면

1. 누른 채 합니다 **Ctrl** 키, 컨트롤을 선택 합니다 [도구 상자 창](/visualstudio/ide/reference/toolbox)합니다.

1. 릴리스를 **Ctrl** 키 및 특정 컨트롤을 추가 하려는 만큼 대화 상자를 선택 합니다.

1. 키를 눌러 **Esc** 컨트롤을 배치를 중지 합니다.

## <a name="to-size-a-control-while-you-add-it"></a>컨트롤을 추가할 때 크기

1. 컨트롤을 선택 합니다 [도구 상자 창](/visualstudio/ide/reference/toolbox)합니다.

1. 대화 상자에 새 컨트롤의 왼쪽 위 모퉁이 만들려는 (십자)는 커서를 놓습니다.

1. 선택 하 고 대화 상자에서 컨트롤의 왼쪽 위 모퉁이 고정 하려면 마우스 단추를 누른 후 컨트롤의 원하는 크기가 될 때까지 커서를 오른쪽 아래로 끕니다.

   > [!NOTE]
   > 실제로 그릴 컨트롤의 네 모퉁이 고정할 수 있습니다. 이 절차 예를 들어 왼쪽 위 모퉁이 사용 합니다.

1. 마우스 단추를 놓습니다. 컨트롤의 대화 상자에서 지정한 크기에 도달 합니다.

   > [!TIP]
   > 컨트롤의 테두리의 크기 조정 핸들을 이동 하 여 대화 상자에 끌어다 놓으면 후 컨트롤 크기를 조정할 수 있습니다. 자세한 내용은 [개별 컨트롤 크기 조정](../windows/sizing-individual-controls.md)합니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고 항목

[대화 상자의 컨트롤](../windows/controls-in-dialog-boxes.md)<br/>
[대화 상자 컨트롤에 사용할 이벤트 처리기 추가](../windows/adding-event-handlers-for-dialog-box-controls.md)<br/>
[대화 상자 컨트롤 및 변수 형식](../ide/dialog-box-controls-and-variable-types.md)<br/>
[컨트롤](../mfc/controls-mfc.md)<br/>
[컨트롤 클래스](../mfc/control-classes.md)<br/>
[대화 상자 클래스](../mfc/dialog-box-classes.md)<br/>
[스크롤 막대 스타일](../mfc/reference/styles-used-by-mfc.md#scroll-bar-styles)<br/>
[Rich Edit 컨트롤 예](../mfc/rich-edit-control-examples.md)<br/>
