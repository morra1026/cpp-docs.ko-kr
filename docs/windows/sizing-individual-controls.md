---
title: 컨트롤 크기 조정
ms.date: 11/04/2016
f1_keywords:
- vc.editors.dialog.combo
helpviewer_keywords:
- Size to Content command
- size, controls
- text, autosizing controls to fit text
- controls [C++], sizing
- Make Same Size command
- combo boxes, sizing
- list controls [C++], scroll bar width
- CListBox::SetHorizontalExtent
- controls [C++], scroll bar
- scroll bars [C++], displaying in controls
- horizontal scroll bar width
- CListBox class, scroll bar width
- scroll bars [C++], width
ms.assetid: 14ccba02-7171-463a-a121-7018cf1e2e5a
ms.openlocfilehash: a6381dcf1aeb9f73ac3b656229d9332df2a6a519
ms.sourcegitcommit: 52c05e10b503e834c443ef11e7ca1987e332f876
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/05/2019
ms.locfileid: "55742715"
---
# <a name="sizing-controls"></a>컨트롤 크기 조정

컨트롤의 크기를 조정 하려면 크기 조정 핸들을 사용 합니다. 크기 조정 핸들의 포인터가 셰이프 컨트롤을 조정할 수 있는 방향을 가리키도록 변경 됩니다. 현재 크기 조정 핸들은 실선입니다. 크기 조정 핸들을 속이 빈 경우 컨트롤이 해당 축을 따라 크기 조정할 수 없습니다.

또한 가이드 또는 여백 컨트롤 스냅 하 여 컨트롤의 크기를 변경할 수 있습니다 또는 하나 이동 하 여 기본 컨트롤 및 다른에서 가이드입니다.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대한 내용은 [데스크톱 앱에 대한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)를 참조하세요. 관리되는 앱의 전역화 및 지역화 리소스에 대한 내용은 [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index)을 참조하세요.

## <a name="to-size-an-individual-control"></a>개별 컨트롤의 크기

1. 컨트롤을 선택 합니다.

1. 컨트롤의 크기를 변경 하려면 크기 조정 핸들을 끕니다.

   - 위와 옆에 있는 크기 조정 핸들 가로 또는 세로 크기를 변경 합니다.

   - 모퉁이에 크기 조정 핸들 가로 및 세로 크기를 변경합니다.

   > [!TIP]
   > 누른 여 한 번에 하나의 대화 상자 단위 (DLU) 컨트롤을 조정할 수 있습니다는 **Shift** 키 및 사용 하 여는 **오른쪽 화살표** 하 고 **아래쪽 화살표** 키입니다.

## <a name="to-automatically-size-a-control-to-fit-the-text-within-it"></a>자동으로 그 텍스트에 맞게 컨트롤의 크기

선택할 **콘텐츠 크기를 조정** 에서 합니다 **형식** 메뉴.

\- 또는 -

선택한 컨트롤을 마우스 오른쪽 단추로 클릭 **콘텐츠 크기를 조정** 바로 가기 메뉴에서.

## <a name="to-make-controls-the-same-width-height-or-size"></a>확인 하기 위해 동일한 너비, 높이 또는 크기 제어

기준 컨트롤의 크기를 기준으로 하는 컨트롤 그룹의 크기를 조정할 수 있습니다.

1. [컨트롤 선택](../windows/selecting-multiple-controls.md) 크기를 조정 하려면.

   시리즈의 처음 선택 된 컨트롤에는 주요 컨트롤이입니다. 그룹에 있는 컨트롤의 최종 크기 기준 컨트롤의 크기에 따라 달라 집니다. 기준 컨트롤 선택에 대 한 자세한 내용은 참조 하세요. [기준 컨트롤 지정](../windows/specifying-the-dominant-control.md)합니다.

1. **형식** 메뉴 선택 **같은 크기로**, 다음 명령 중 하나를 선택 합니다.

   - **Both**

   - **높이**

   - **너비**

## <a name="to-set-the-size-of-the-combo-box-and-its-drop-down-list"></a>상자 및 드롭다운 목록의 콤보의 크기를 설정 하려면

대화 상자에 추가할 때 콤보 상자 크기. 또한 드롭다운 목록 상자의 크기를 지정할 수 있습니다. 자세한 내용은 [콤보 상자 컨트롤에 추가 값](../windows/adding-values-to-a-combo-box-control.md)합니다.

### <a name="to-size-a-combo-box"></a>콤보 상자 크기

1. 대화 상자에서 콤보 상자 컨트롤을 선택 합니다.

   처음에 오른쪽 및 왼쪽 크기 조정 핸들만 활성화 됩니다.

1. 콤보 상자의 너비를 설정 하려면 크기 조정 핸들을 사용 합니다.

또한 콤보 상자의 드롭다운 부분이의 세로 크기를 설정할 수 있습니다.

### <a name="to-set-the-size-of-the-combo-box-drop-down-list"></a>드롭다운 목록 상자 콤보의 크기를 설정 하려면

1. 콤보 상자의 오른쪽에 있는 드롭다운 화살표 단추를 선택 합니다.

   ![MFC 프로젝트에서 콤보 상자에서 화살표](../mfc/media/vccomboboxarrow.gif "vcComboBoxArrow")

   드롭다운 목록에서 영역이 확장을 사용 하 여 콤보 상자의 크기를 표시 하려면 해당 컨트롤의 개요입니다.

1. 드롭다운 목록에서 영역의 초기 크기를 변경 하려면 아래쪽 크기 조정 핸들을 사용 합니다.

   ![콤보&#45;MFC 프로젝트의 상자 크기 조정](../mfc/media/vccomboboxsizing.gif "vcComboBoxSizing")

1. 콤보 상자의 드롭다운 목록에서 일부를 다시 드롭다운 화살표를 선택 합니다.

## <a name="to-set-the-width-of-a-horizontal-scroll-bar-and-make-it-appear"></a>가로 스크롤 막대의 너비를 설정 하 고 표시 되도록 하려면

MFC 클래스를 사용 하 여 대화 상자에 가로 스크롤 막대를 사용 하 여 목록 상자에 추가한 경우 스크롤 막대를 응용 프로그램에 자동으로 나타나지 않습니다.

호출 하 여 광범위 한 요소에 대 한 최대 너비를 설정할 [CListBox::SetHorizontalExtent](../mfc/reference/clistbox-class.md#sethorizontalextent) 코드에서.

   이 값을 설정 하지 않고 스크롤 막대 표시 되지도 목록 상자의 항목 상자 보다 넓을 경우.
> [!NOTE]
> 가로 스크롤 막대에는 MFC에 필요합니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고자료

[대화 상자의 컨트롤](../windows/controls-in-dialog-boxes.md)<br/>
[컨트롤](../mfc/controls-mfc.md)
