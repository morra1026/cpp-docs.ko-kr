---
title: '아이콘 및 커서: (아이콘에 대 한 c + + 이미지 편집기) 디스플레이 장치용 이미지 리소스'
ms.date: 11/04/2016
f1_keywords:
- vc.editors.icon
- vc.editors.newimagetype
- vc.editors.customimage
- vc.editors.opendeviceimage
- vc.editors.image.editing
helpviewer_keywords:
- cursors [C++], creating
- image resources [C++], display devices
- icons [C++], creating
- cursors [C++], types
- icons [C++]
- Image editor [C++], icons and cursors
- cursors [C++]
- display devices [C++], creating icons for
- cursors [C++], hot spots
- icons [C++], types
- icons [C++], creating
- display devices [C++], creating image
- images [C++], creating for display devices
- icons [C++], inserting
- New <Device> Image Type dialog box [C++]
- Custom Image dialog box [C++]
- Open <Device> Image dialog box [C++]
- New Device Image command
- display devices [C++], adding images
- cursors [C++], adding
- icons, adding
- display devices [C++], copying images
- cursors [C++], copying
- icons, copying
- cursors [C++], deleting
- display devices [C++], deleting device image
- icons, erasing
- icons, deleting
- cursors [C++], undoing changes
- icons, undoing changes
- cursors [C++], screen regions
- inverse colors [C++], device images
- transparent regions, device images
- transparency, device images
- Image editor [C++], device images
- inverse regions, device images
- cursors [C++], transparent regions
- screen colors
- regions, transparent
- icons [C++], transparent regions
- display devices [C++], transparent and screen regions
- transparent regions in devices
- regions, inverse
- colors [C++], Image editor
- device projects [C++], transparent images
- icons [C++], screen regions
- 256-color palette
- cursors [C++], color
- colors [C++], icons
- colors [C++], cursors
- icons, color
- colors [C++], icons and cursors
- color palettes, 256-color
- palettes, 256-color
- cursors [C++], hot spots
- hot spots
ms.assetid: 8f0809a8-0cf0-4da9-b23d-51f28bf15f5b
ms.openlocfilehash: 027c3c0380a73c624432bbe45758b3296732949a
ms.sourcegitcommit: bd637e9c39650cfd530520ea978a22fa4caa0e42
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/07/2019
ms.locfileid: "55849947"
---
# <a name="icons-and-cursors-image-resources-for-display-devices-c-image-editor-for-icons"></a>아이콘 및 커서: (아이콘에 대 한 c + + 이미지 편집기) 디스플레이 장치용 이미지 리소스

아이콘 및 커서는 다양한 유형의 디스플레이 디바이스에 맞는 다양한 크기 및 색 구성표의 여러 이미지를 포함할 수 있는 그래픽 리소스입니다. 또한 커서에는 "핫 스폿을" Windows가 사용 하 여 해당 위치를 추적 하는 위치입니다. 아이콘 및 커서 모두 만들어지고 사용 하 여 편집 합니다 **이미지** 편집기, 비트맵 및 기타 이미지는 합니다.

새 아이콘 또는 커서를 만들 때 합니다 **이미지** 편집기는 먼저 표준 형식의 이미지를 만듭니다. 이미지는 처음에 투명한 화면 색상으로 채워집니다. 이미지가 커서인 경우 핫스팟은 처음에 왼쪽 위 모서리(좌표 0, 0)에 있습니다.

기본적으로 **이미지** 편집기는 다음 표에 표시 된 장치의 추가 이미지 만들기를 지원 합니다. [사용자 지정 이미지 대화 상자](custom-image-dialog-box-image-editor-for-icons.md)에 너비, 높이 및 색상 수 매개 변수를 입력하여 기타 장치의 이미지를 만들 수 있습니다.

> [!NOTE]
> 사용 하 여 **이미지 편집기**, 32 비트 이미지를 볼 수 있지만 편집할 수는 없습니다.

|색|너비(픽셀)|높이(픽셀)|
|-----------|----------------------|-----------------------|
|단색|16|16|
|단색|32|32|
|단색|48|48|
|단색|64|64|
|단색|96|96|
|16|16|16|
|16|32|32|
|16|64|64|
|16|48|48|
|16|96|96|
|256|16|16|
|256|32|32|
|256|48|48|
|256|64|64|
|256|96|96|

## <a name="create-a-device-image-icon-or-cursor"></a>(아이콘 또는 커서) 장치 이미지 만들기

새 아이콘 또는 커서 리소스를 만들 때 합니다 **이미지** 편집기 (32 × 32 아이콘에 대 한 16 색 32 × 32, 커서에 대 한 단색) 특정 스타일에서 이미지를 먼저 만듭니다. 그런 다음 초기 아이콘이 나 커서에 다양 한 크기 및 스타일 이미지를 추가 하 고 디스플레이 장치에 대 한 필요에 따라 각 추가 이미지를 편집할 수 있습니다. 또한 기존 이미지 형식에서 또는 그래픽 프로그램에서 만든 비트맵에서 잘라내기 / 붙여넣기 작업을 사용 하 여 이미지를 편집할 수 있습니다.

아이콘 또는 커서 리소스를 열면 합니다 [이미지 편집기](../windows/image-editor-for-icons.md), 기본적으로 열려 대부분의 현재 디스플레이 장치에 밀접 하 게 일치 하는 이미지입니다.

### <a name="new-ltdevicegt-image-type-dialog-box"></a>새 &lt;장치&gt; 이미지 형식 대화 상자

합니다 **새로 만들기 &lt;장치&gt; 이미지 형식** 대화 상자를 사용 하면 지정 된 형식의 새 장치 이미지를 만들 수 있습니다. 열려는 합니다 **새로 만들기 \<장치 > 이미지** 대화 상자에서 **새 이미지 형식** 에 **이미지** 메뉴. 포함 된 다음과 같은 속성을 **대상 이미지 형식** 하 고 **사용자 지정**합니다.

#### <a name="target-image-type"></a>대상 이미지 형식

사용 가능한 이미지 목록을 표시 합니다. 열려는 이미지 형식 선택:

||||
|-|-|-|
|-16x16, 16 가지 색|-48 x 48 16 색|-96 x 96 16 색|
|-16x16, 256 색|-48 x 48 256 색|-96 x 96 256 색|
|-16x16, 단색|- 48 x 48, Monochrome|- 96 x 96, Monochrome|
|-32 x 32 16 색|-64 x 64 16 색||
|-32 x 32 256 색|-64 x 64 256 색||
|부터 단색 32 x 32|-단색 64 x 64||

> [!NOTE]
> 기존 이미지가이 목록에 나타나지 않습니다.

#### <a name="custom"></a>사용자 지정

열립니다는 **사용자 지정 이미지** 대화 상자는 사용자 지정 크기와 색상 수를 사용 하 여 새 이미지를 만들 수 있습니다.

합니다 **사용자 지정 이미지** 대화 상자를 사용 하면 사용자 지정 크기와 색상 수를 사용 하 여 새 이미지를 만들 수 있습니다. 포함 된 다음 속성은 다음과 같습니다.

|속성|설명|
|---|---|
|**너비**|픽셀 (1-512 최대 2048)에서 사용자 지정 이미지의 너비를 입력할 공간을 제공 합니다.|
|**높이**|사용자 지정 이미지 픽셀 (1-512 최대 2048)의 높이 입력할 공간을 제공 합니다.|
|**색**|사용자 지정 이미지에 대 한 색의 수를 선택 하기 위한 공간을 제공 합니다. 2, 16, 또는 256입니다.|

### <a name="open-ltdevicegt-image-dialog-box"></a>오픈 &lt;장치&gt; 이미지 대화 상자

사용 된 **엽니다 &lt;장치&gt; 이미지** c + + 프로젝트에서 장치 이미지를 열려면 대화 상자. 현재 리소스 (현재 리소스의 일부인 이미지)의 기존 장치 이미지를 나열 합니다. 포함 된 속성은:

|속성|설명|
|---|---|
|**현재 이미지**|리소스에 포함 된 이미지를 나열 합니다. 열려는 이미지 유형을 선택 합니다.|

### <a name="to-create-a-new-icon-or-cursor"></a>새 아이콘 또는 커서를 만들려면

1. [리소스 뷰](../windows/resource-view-window.md),.rc 파일을 마우스 오른쪽 단추로 클릭 한 다음 선택 **삽입 리소스** 바로 가기 메뉴에서. (단추로 cursor와 같은.rc 파일에서 기존 이미지 리소스가 이미 있는 경우는 **커서** 선택한 폴더 **커서 삽입** 바로 가기 메뉴에서.)

   > [!NOTE]
   > 참조 프로젝트에.rc 파일이 없으면 [새 리소스 스크립트 파일 만들기](../windows/how-to-create-a-resource-script-file.md)합니다.

1. 에 [리소스 삽입 대화 상자](../windows/add-resource-dialog-box.md)를 선택 **아이콘** 또는 **커서** 선택한 **새**합니다. 아이콘에 대 한이 작업은 32 × 32를 16 색 아이콘을 사용 하 여 아이콘 리소스를 만듭니다. 커서의 경우 32 × 32 단색 (2-색) 이미지가 생성 됩니다.

   더하기 기호 (**+**)에서 이미지 리소스 형식을 옆에 표시 되는 **삽입 리소스** 대화 상자, 즉 모음 템플릿을 사용할 수 있습니다. 템플릿의 목록을 확장 하는 템플릿을 선택 하 고 선택 하려면 더하기 기호 **새로 만들기**합니다.

## <a name="add-an-image-for-a-different-display-device"></a>다른 디스플레이 장치용 이미지 추가

1. 에 **이미지** 메뉴에서 **새 장치 이미지** (마우스 오른쪽 단추로 클릭 하거나는 **이미지 편집기** 창 선택 **새 장치 이미지** 에서 바로 가기 메뉴)입니다.

1. 추가 하려는 이미지의 유형을 선택 합니다. 선택할 수도 있습니다 **사용자 지정** 크기가 기본 목록에서 사용할 수 없는 아이콘을 만들려고 합니다.

## <a name="copy-a-device-image"></a>장치 이미지 복사

1. 에 **이미지** 메뉴에서 **장치 이미지 열기** 현재 이미지 목록에서 이미지를 선택 합니다. 예를 들어 32 × 32, 16 색 버전의 아이콘을 선택 합니다.

1. 현재 표시 된 아이콘 이미지 복사 (**Ctrl**+**C**).

1. 다른 아이콘의 다른 이미지를 엽니다 **이미지 편집기** 창입니다. 예를 들어 16 × 16, 아이콘의 16 색 버전을 엽니다.

1. 아이콘 이미지를 붙여 넣습니다 (**Ctrl**+**V**) 간에 **이미지 편집기** 다른 창입니다. 더 큰 크기를 더 작은 크기에 붙여넣을 경우 이미지 크기를 조정 하는 아이콘 핸들을 사용할 수 있습니다.

## <a name="delete-a-device-image"></a>장치 이미지 삭제

아이콘 이미지에 표시 되는 동안 합니다 **이미지** 편집기 선택 **장치 이미지 삭제** 에서 합니다 **이미지** 메뉴. 리소스의 마지막 아이콘 이미지를 삭제 하면 리소스가 삭제 됩니다.

   > [!NOTE]
   > 누를 때 합니다 **Del** 키, 이미지 및 아이콘 그린 색 삭제는 남아 있지만 이제 디자인할 수 있습니다. 키를 누르면 **Del** 눌러도 실수로 **Ctrl**+**Z** 작업을 취소 하 합니다.

## <a name="create-transparent-or-inverse-regions-in-device-images"></a>장치 이미지에서 투명 하 게 또는 반전 영역 만들기

에 [이미지 편집기](../windows/image-editor-for-icons.md), 초기 아이콘 또는 커서 이미지의 특성은 투명 합니다. 아이콘 및 커서 이미지는 사각형, 대부분 표시 되지 않습니다 있도록 이미지 부분; 투명 하 게 되므로 아이콘 또는 커서를 통해 화면에서 기본 이미지를 보여 줍니다. 아이콘을 끌어 이미지의 부분 반전된 된 색으로 나타날 수 있습니다. 화면색 및 반전색에서 설정 하 여 이러한 효과 낼 합니다 [색 창](../windows/colors-window-image-editor-for-icons.md)합니다.

아이콘의 화면 및 역 색을 적용 하 고 커서 셰이프 및 파생된 이미지 색 또는 반전 영역을 할당 합니다. 색은 해당 특성이 있는 이미지의 부분을 나타냅니다. 편집 화면색 및 반전색 특성을 나타내는 색을 변경할 수 있습니다. 이러한 변경 내용은 아이콘이 나 응용 프로그램에서 커서의 모양에 영향을 주지 않습니다.

> [!NOTE]
> 표시되는 대화 상자와 메뉴 명령은 활성 설정 또는 버전에 따라 **도움말**에 설명된 것과 다를 수 있습니다. 설정을 변경하려면 **도구** 메뉴에서 **설정 가져오기 및 내보내기** 를 선택합니다. 자세한 내용은 [Visual Studio IDE 개인 설정](/visualstudio/ide/personalizing-the-visual-studio-ide)을 참조하세요.

### <a name="to-create-transparent-or-inverse-regions"></a>투명 또는 반전 영역을 만드는 데

1. 에 **색** 창에서 합니다 **화면색** 선택기 또는 **반전색** 선택기입니다.

1. 화면 또는 반전색 그리기 도구를 사용 하 여 이미지에 적용 됩니다. 그리기 도구에 대 한 자세한 내용은 참조 하세요. [그리기 도구를 사용 하 여](using-a-drawing-tool-image-editor-for-icons.md)입니다.

### <a name="to-change-the-screen-or-inverse-color"></a>화면 또는 역 색을 변경 하려면

1. 중 하나를 선택 합니다 **화면색** 선택기 또는 **반전색** 선택기입니다.

1. 색을 선택 합니다 **색** 색상표에는 **색** 창입니다.

   보완 색상 다른 선택기에 대 한 자동으로 할당 됩니다.

   > [!TIP]
   > 두 번 클릭 합니다 **화면색** 또는 **반전색** 선택기를 [사용자 지정 색 선택 대화 상자](../windows/custom-color-selector-dialog-box-image-editor-for-icons.md) 나타납니다.

## <a name="use-the-256-color-palette"></a>256 색상표 사용

사용 하 여 **이미지** 편집기, 아이콘 및 커서 선택할 256 색 색상표를 사용 하 여 크기가 큰 (64 × 64) 될 수 있습니다. 리소스를 만든 후 장치 이미지 스타일을 선택 합니다.

### <a name="to-create-a-256-color-icon-or-cursor"></a>256 색 아이콘이 나 커서를 만들려면

1. [리소스 뷰](../windows/resource-view-window.md),.rc 파일을 마우스 오른쪽 단추로 클릭 한 다음 선택 **삽입 리소스** 바로 가기 메뉴에서. (단추로 cursor와 같은.rc 파일에서 기존 이미지 리소스가 이미 있는 경우는 **커서** 선택한 폴더 **커서 삽입** 바로 가기 메뉴에서.)

   > [!NOTE]
   > 프로젝트에 .rc 파일이 아직 없는 경우 [새 리소스 스크립트 파일 만들기](../windows/how-to-create-a-resource-script-file.md)를 참조하세요.

1. 에 [리소스 삽입 대화 상자](../windows/add-resource-dialog-box.md)를 선택 **아이콘** 또는 **커서** 선택한 **새**합니다.

1. 에 **이미지** 메뉴에서 **새 장치 이미지**합니다.

1. 원하는 256 색 이미지 스타일을 선택 합니다.

### <a name="to-choose-a-color-from-the-256-color-palette-for-large-icons"></a>큰 아이콘에 대 한 256 색상표에서 색을 선택 하려면

그릴을 선택 하 여 256 색상표에서 색을 선택 해야 합니다 **색** 색상표에는 [색 창](../windows/colors-window-image-editor-for-icons.md)합니다.

1. 큰 아이콘 또는 커서를 선택 하거나 새 큰 아이콘 또는 커서를 만듭니다.

1. 에 표시 된 256 색에서 색을 선택 합니다 **색** 색상표에는 **색** 창입니다.

   선택한 색은 현재 색으로 표시 됩니다는 **색** 색상표에는 **색** 창입니다.

   > [!NOTE]
   > 256 컬러 이미지에 사용 되는 초기 색상표를 반환한 색상표와 일치 하는 `CreateHalftonePalette` Windows API입니다. Windows shell을 위한 모든 아이콘 색상표 인식 하는 동안 깜박임을 방지 하기 위해이 색상표를 사용 해야 합니다.

## <a name="set-a-cursor39s-hot-spot"></a>커서를 설정&#39;s 핫 스폿

커서의 핫 스폿 지점인 Windows 커서의 위치를 추적에서 참조 하 합니다. 기본적으로 핫 스폿 커서 (좌표 0, 0)의 왼쪽 위 모퉁이에 설정 됩니다. 합니다 **핫스팟** 속성에는 [속성 창](/visualstudio/ide/reference/properties-window) 핫스폿 좌표가 표시 합니다.

### <a name="to-set-a-cursors-hot-spot"></a>커서의 핫스팟 설정

1. 에 [이미지 편집기 도구 모음](../windows/toolbar-image-editor-for-icons.md)를 선택 합니다 **핫스팟 설정** 도구입니다.

1. 커서의 핫 스폿으로 할당할 픽셀을 선택 합니다.

   합니다 **핫스팟** 속성에는 **속성** 창에 새 좌표로 표시 됩니다.

   > [!TIP]
   > 도구 모음 단추 위로 커서를 올려 놓으면 도구 설명이 표시 됩니다. 이러한 팁 각 단추의 기능을 식별할 수 있습니다.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대한 내용은 [데스크톱 앱에 대한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)를 참조하세요. 관리되는 앱의 전역화 및 지역화 리소스에 대한 내용은 [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index)을 참조하세요.

## <a name="requirements"></a>요구 사항

없음

## <a name="see-also"></a>참고자료

[이미지 메뉴](../windows/image-menu-image-editor-for-icons.md)<br/>
[아이콘에 대한 이미지 편집기](../windows/image-editor-for-icons.md)<br/>
[아이콘](/windows/desktop/menurc/icons)<br/>
[커서](/windows/desktop/menurc/cursors)<br/>
[액셀러레이터 키](../windows/accelerator-keys-image-editor-for-icons.md)<br/>
