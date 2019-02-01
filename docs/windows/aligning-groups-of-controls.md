---
title: 컨트롤 맞춤
ms.date: 11/04/2016
helpviewer_keywords:
- controls [C++], aligning
- controls [C++], positioning
- Space Evenly command
- dialog box controls [C++], placement
- Center in Dialog command
- Arrange Buttons command
- buttons, arranging push buttons in dialog boxes
- push buttons
ms.assetid: a4f49a73-4a17-44b3-8568-aa35f646b5cf
ms.openlocfilehash: abfae0f0146fa736a6427eb1180805717ce8a78e
ms.sourcegitcommit: 5270117dbecc4c49bca0cf10b927bae3c9930038
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/31/2019
ms.locfileid: "55484983"
---
# <a name="align-controls"></a>컨트롤 맞춤

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대한 내용은 [데스크톱 앱에 대한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)를 참조하세요. 관리되는 앱의 전역화 및 지역화 리소스에 대한 내용은 [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index)을 참조하세요.

다음 절차에서는 컨트롤을 정렬 하는 방법을 보여 줍니다.

## <a name="to-align-groups-of-controls"></a>컨트롤의 그룹에 맞게

1. [컨트롤 선택](../windows/selecting-multiple-controls.md) 정렬 해야 합니다. 기준 컨트롤을 먼저 되도록 하려는 컨트롤을 선택 해야 하거나 맞춤을 실행 하거나 명령 크기를 조정 하기 전에 주요 컨트롤 수를 설정 합니다.

   컨트롤 그룹의 최종 위치 기준 컨트롤의 위치에 따라 달라 집니다. 기준 컨트롤 선택에 대 한 자세한 내용은 참조 하세요. [기준 컨트롤 지정](../windows/specifying-the-dominant-control.md)합니다.

1. **형식** 메뉴 선택 **Align**, 맞춤 다음 방법 중 하나를 선택:

   - `Lefts`: 선택한 컨트롤을 왼쪽으로 맞춥니다.

   - `Centers`: 선택한 컨트롤의 가운데 일렬로 가로로 맞춥니다.

   - `Rights`: 선택한 컨트롤의 오른쪽 면 일렬로 정렬 합니다.

   - `Tops`: 위쪽 가장자리를 따라 선택된 된 컨트롤에 맞춥니다.

   - `Middles`: 선택한 컨트롤의 중간 일렬로 세로로 맞춥니다.

   - `Bottoms`: 아래쪽 가장자리를 따라 선택된 된 컨트롤에 맞춥니다.

## <a name="to-even-the-spacing-between-controls"></a>컨트롤 사이의 간격을 일정

합니다 **대화 상자** 편집기 선택한 가장 바깥쪽 컨트롤 간에 균등 하 게 공간 컨트롤에 있습니다.

1. 다시 정렬 하려면 컨트롤을 선택 합니다.

1. **형식** 메뉴 선택 **균등 하 게 공간**, 다음 간격 맞춤 중 하나를 선택 하 고:

   - `Across`: 컨트롤 맨 왼쪽 및 오른쪽에 있는 선택 된 컨트롤 간에 균등 하 게 공간입니다.

   - `Down`: 컨트롤 맨 위 및 맨 아래 선택 된 컨트롤 간에 균등 하 게 공간입니다.

## <a name="to-center-controls-in-a-dialog-box"></a>대화 상자에서 컨트롤 가운데

1. 컨트롤이 나 컨트롤 다시 정렬 하려면 선택 합니다.

1. **형식** 메뉴 선택 **센터에서 대화 상자**, 다음 배치 방법 중 하나를 선택 하 고:

   - `Vertical`: 컨트롤 대화 상자에서 세로 방향으로 가운데 맞춤 합니다.

   - `Horizontal`: 컨트롤 대화 상자에서 가로 방향으로 가운데 맞춤 합니다.

## <a name="to-arrange-push-buttons-along-the-right-or-bottom-of-a-dialog-box"></a>오른쪽 또는 아래쪽 대화 상자의 누름 단추 정렬 하려면

1. 하나 이상의 푸시 단추를 선택 합니다.

1. **형식** 메뉴 선택 **단추 정렬**, 다음 배치 방법 중 하나를 선택 하 고:

   - `Right`: 대화 상자의 오른쪽 가장자리를 따라 누름 단추를 배치 합니다.

   - `Bottom`: 대화 상자의 아래쪽 가장자리를 따라 누름 단추를 배치 합니다.

       누름 단추 이외의 컨트롤을 선택할 위치로 영향을 받지 않습니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고 항목

[대화 상자에 컨트롤 배치](../windows/arrangement-of-controls-on-dialog-boxes.md)<br/>
[대화 상자의 컨트롤](../windows/controls-in-dialog-boxes.md)<br/>
[컨트롤](../mfc/controls-mfc.md)