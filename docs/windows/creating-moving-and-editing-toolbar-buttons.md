---
title: 만들기, 이동 및 편집 도구 모음 단추 (c + +)
ms.date: 11/04/2016
f1_keywords:
- vc.editors.toolbar
helpviewer_keywords:
- buttons [C++], custom toolbars
- toolbar buttons [C++], editing
- buttons
- toolbar buttons [C++], creating
- Toolbar editor [C++], creating buttons
- toolbar buttons [C++], button image
- toolbar buttons [C++], creating
- toolbar buttons (in Toolbar editor)
- toolbar buttons [C++], moving
- Toolbar editor [C++], moving buttons
- Toolbar editor [C++], copying buttons
- toolbars [C++], copying buttons
- toolbar buttons [C++], copying
- toolbar buttons [C++], deleting
- Toolbar editor [C++], deleting buttons
- Toolbar editor [C++], spacing toolbar buttons
- toolbar buttons [C++], space between buttons
- toolbar controls [MFC], command ID
- toolbar buttons [C++], setting properties
- Toolbar editor [C++], toolbar button properties
- command IDs, toolbar buttons
- size, toolbar buttons
- toolbar buttons [C++], setting properties
- Toolbar editor [C++], toolbar button properties
- status bars [C++], active toolbar button text
- command IDs, toolbar buttons
- width, toolbar buttons
ms.assetid: d0f0c6c6-9d7e-42b5-a86a-7558127386e7
ms.openlocfilehash: 2a67123e444ad208eaae74a24b72288f2dbb3bdb
ms.sourcegitcommit: 52c05e10b503e834c443ef11e7ca1987e332f876
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/05/2019
ms.locfileid: "55742702"
---
# <a name="creating-moving-and-editing-toolbar-buttons-c"></a>만들기, 이동 및 편집 도구 모음 단추 (c + +)

있습니다 수 쉽게 만들기, 이동, 복사 및 편집 도구 모음 단추입니다.

기본적으로 도구 모음의 오른쪽 끝에서 공백 또는 새 단추가 표시 됩니다. 편집 하기 전에이 단추를 이동할 수 있습니다. 새 단추를 만들면 다른 빈 단추 편집 단추 오른쪽에 나타납니다. 도구 모음을 저장 하면 빈 단추 저장 되지 않습니다.

도구 모음 단추의 속성을 다음과 같습니다.

|속성|Description|
|--------------|-----------------|
|**ID**|단추에 대 한 ID를 정의합니다. 드롭다운 목록에는 일반적인 나와 **ID** 이름입니다.|
|**너비**|단추의 너비를 설정합니다. 16 픽셀을 사용 하는 것이 좋습니다.|
|**높이**|단추의 높이 설정합니다. 도구 모음에서 모든 단추의 높이 변경 하는 하나의 단추의 높이입니다. 15 픽셀을 사용 하는 것이 좋습니다.|
|**프롬프트**|상태 표시줄에 표시 되는 메시지를 정의 합니다. 도구 모음 단추를 도구 설명 추가 \n 및 이름을 추가 합니다. 자세한 내용은 [도구 설명을 만드는](../windows/creating-a-tool-tip-for-a-toolbar-button.md)합니다.|

**너비** 하 고 **높이** 모든 단추에 적용 합니다. 도구 모음을 만드는 데 사용 되는 비트맵은 2048의 최대 너비입니다. 따라서 단추 너비를 512로 설정 하는 경우 수만 단추 4 개 있고 513를 너비를 설정 하면 세 개의 단추만 넣을 수 있습니다.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대한 내용은 [데스크톱 앱에 대한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)를 참조하세요. 관리되는 앱의 전역화 및 지역화 리소스에 대한 내용은 [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index)을 참조하세요.

다음 작업을 참조 하세요.

## <a name="to-create-a-new-toolbar-button"></a>새 도구 모음 단추를 만들려면

1. [리소스 뷰](../windows/resource-view-window.md) 리소스 폴더를 확장 (예를 들어 *: Project1.rc*).

   > [!NOTE]
   > 프로젝트에 .rc 파일이 아직 없는 경우 [새 리소스 스크립트 파일 만들기](../windows/how-to-create-a-resource-script-file.md)를 참조하세요.

1. 확장 된 **도구 모음** 폴더를 편집 하려면 도구 모음을 선택 합니다.

1. 도구 모음의 오른쪽 끝에 빈 단추에는 ID를 할당 합니다. 편집 하 여 수행할 수는 **ID** 속성에는 [속성 창](/visualstudio/ide/reference/properties-window)합니다. 예를 들어, 다음 도구 모음 단추 메뉴 옵션으로 동일한 ID를 제공 하는 것이 좋습니다. 이 경우 드롭다운 목록 상자를 사용 하 여 선택 합니다 **ID** 메뉴 옵션입니다.

   또는

   도구 모음의 오른쪽 끝에 비어 있는 단추를 선택 (에 **도구 모음 보기** 창) 고 그리기를 시작 합니다. 기본 단추 명령 ID가 할당 됩니다 (ID_BUTTON\<n >).

또한 복사 하 고 새 단추 여 도구 모음 이미지를 붙여넣을 수 있습니다.

## <a name="to-add-an-image-to-a-toolbar-as-a-button"></a>도구 모음에 단추와 이미지를 추가 하려면

1. [리소스 뷰](../windows/resource-view-window.md)를 두 번 클릭 하 여 도구 모음을 엽니다.

1. 다음으로, 도구 모음에 추가 하려는 이미지를 엽니다.

   > [!NOTE]
   > Visual Studio에서 이미지를 열면에서 열립니다는 **이미지** 편집기입니다. 또한 다른 그래픽 프로그램에서 이미지를 열 수 있습니다.

1. **편집할** 메뉴에서 선택 **복사**합니다.

1. 소스 창의 맨 위에 있는 해당 탭을 선택 하 여 도구 모음을 전환 합니다.

1. **편집할** 메뉴 선택 **붙여넣기**합니다.

   이미지는 새 단추도 도구 모음에 표시 됩니다.

## <a name="to-move-a-toolbar-button"></a>도구 모음 단추 이동 하려면

에 **도구 모음 보기** 창 도구 모음에서 새 위치로 이동 하려면 단추를 끌어 옵니다.

## <a name="to-copy-buttons-from-a-toolbar"></a>도구 모음에서 단추 복사

1. 누른 합니다 **Ctrl** 키입니다.

1. 에 **도구 모음 보기** 창 끌거나 단추 중 하나를 새 위치로 도구 모음에서 위치에 다른 도구 모음에서 합니다.

## <a name="to-delete-a-toolbar-button"></a>도구 모음 단추를 삭제 하려면

도구 모음 단추를 선택 하 고 도구 모음 밖으로 끕니다.

## <a name="to-insert-or-remove-space-between-buttons-on-a-toolbar"></a>삽입 하거나 도구 모음에서 단추 사이의 공백 제거

일반적으로 단추 사이 공백을 삽입할 끌어 다른 도구 모음에서 합니다. 공간을 제거 하려면 다른 쪽으로 끌어 옵니다.

### <a name="to-insert-a-space-before-a-button-that-isnt-followed-by-a-space"></a>뒤에 공백이 없습니다 단추 앞에 공백을 삽입 하려면

오른쪽 단추를 끌거나 겹치는 다음 단추에 대 한 중간 될 때까지 아래로 합니다.

### <a name="to-insert-a-space-before-a-button-that-is-followed-by-a-space-and-to-keep-the-trailing-space"></a>공백 뒤에 나오는 단추 앞에 공백을 삽입 하 고 후행 공백을 유지 합니다.

오른쪽 가장자리나 아래쪽 가장자리 다음 단추 바로 겹쳐질 때까지 단추를 끕니다.

### <a name="to-insert-a-space-before-a-button-that-is-followed-by-a-space-and-close-up-that-following-space"></a>다음 해당 공간을 닫고 공백 뒤에 나오는 단추 앞에 공백을 삽입 하려면

오른쪽 단추를 끌거나 겹치는 다음 단추에 대 한 중간 될 때까지 아래로 합니다.

### <a name="to-remove-a-space-between-buttons-on-a-toolbar"></a>도구 모음의 단추 사이 공백을 제거 하려면

중간에 대 한 다음 단추와 겹칠 때까지 공간의 다른 쪽에 있는 단추로 공간 한쪽 단추를 끕니다.

   다른 위치로 끌어 온 다음 단추 공간이 없을 경우 끌면 단추 옆에 있는 단추를 반 이상 합니다 **도구 모음** 편집기에는 또한 수 있는 단추의 반대쪽에 공백을 삽입 끕니다.

## <a name="to-change-the-properties-of-a-toolbar-button"></a>도구 모음 단추의 속성을 변경 하려면

1. C + + 프로젝트의 도구 모음 단추를 선택 합니다.

1. 에 새 ID를 입력 합니다 **ID** 속성에는 [속성 창](/visualstudio/ide/reference/properties-window), 드롭 다운 목록을 사용 하 여 새 선택 또는 **ID**합니다.

## <a name="requirements"></a>요구 사항

MFC 또는 ATL

## <a name="see-also"></a>참고 항목

[도구 모음 편집기](../windows/toolbar-editor.md)
