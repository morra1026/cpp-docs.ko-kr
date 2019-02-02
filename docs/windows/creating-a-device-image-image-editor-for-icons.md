---
title: 장치 이미지 만들기(아이콘에 대한 이미지 편집기)
ms.date: 11/04/2016
f1_keywords:
- vc.editors.icon
- vc.editors.newimagetype
- vc.editors.customimage
- vc.editors.opendeviceimage
helpviewer_keywords:
- cursors [C++], creating
- icons [C++], creating
- display devices [C++], creating image
- images [C++], creating for display devices
- icons [C++], inserting
- New <Device> Image Type dialog box [C++]
- Custom Image dialog box [C++]
- Open <Device> Image dialog box [C++]
ms.assetid: 5a536928-32df-4ace-beb1-1521ce3b871f
ms.openlocfilehash: ce1069f6f410d7a60d631461086ca8870ef679c0
ms.sourcegitcommit: efcc8c97570ddf7631570226c700e8f6ebb6c7be
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/01/2019
ms.locfileid: "55560298"
---
# <a name="creating-a-device-image-image-editor-for-icons"></a>장치 이미지 만들기(아이콘에 대한 이미지 편집기)

새 아이콘 또는 커서 리소스를 만들 때 합니다 **이미지** 편집기 (32 × 32 아이콘에 대 한 16 색 32 × 32, 커서에 대 한 단색) 특정 스타일에서 이미지를 먼저 만듭니다. 그런 다음 초기 아이콘이 나 커서에 다양 한 크기 및 스타일 이미지를 추가 하 고 디스플레이 장치에 대 한 필요에 따라 각 추가 이미지를 편집할 수 있습니다. 또한 기존 이미지 형식에서 또는 그래픽 프로그램에서 만든 비트맵에서 잘라내기 / 붙여넣기 작업을 사용 하 여 이미지를 편집할 수 있습니다.

아이콘 또는 커서 리소스를 열면 합니다 [이미지 편집기](../windows/image-editor-for-icons.md), 기본적으로 열려 대부분의 현재 디스플레이 장치에 밀접 하 게 일치 하는 이미지입니다.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대한 내용은 [데스크톱 앱에 대한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)를 참조하세요. 관리되는 앱의 전역화 및 지역화 리소스에 대한 내용은 [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index)을 참조하세요.

## <a name="new-ltdevicegt-image-type-dialog-box"></a>새 &lt;장치&gt; 이미지 형식 대화 상자

합니다 **새로 만들기 &lt;장치&gt; 이미지 형식** 대화 상자를 사용 하면 지정 된 형식의 새 장치 이미지를 만들 수 있습니다. 열려는 합니다 **새로 만들기 \<장치 > 이미지** 대화 상자에서 **새 이미지 형식** 에 **이미지** 메뉴. 포함 된 다음과 같은 속성을 **대상 이미지 형식** 하 고 **사용자 지정**합니다.

### <a name="target-image-type"></a>대상 이미지 형식

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

### <a name="custom"></a>사용자 지정

열립니다는 **사용자 지정 이미지** 대화 상자는 사용자 지정 크기와 색상 수를 사용 하 여 새 이미지를 만들 수 있습니다.

합니다 **사용자 지정 이미지** 대화 상자를 사용 하면 사용자 지정 크기와 색상 수를 사용 하 여 새 이미지를 만들 수 있습니다. 포함 된 다음 속성은 다음과 같습니다.

|속성|설명|
|---|---|
|**너비**|픽셀 (1-512 최대 2048)에서 사용자 지정 이미지의 너비를 입력할 공간을 제공 합니다.|
|**높이**|사용자 지정 이미지 픽셀 (1-512 최대 2048)의 높이 입력할 공간을 제공 합니다.|
|**색**|사용자 지정 이미지에 대 한 색의 수를 선택 하기 위한 공간을 제공 합니다. 2, 16, 또는 256입니다.|

## <a name="open-ltdevicegt-image-dialog-box"></a>오픈 &lt;장치&gt; 이미지 대화 상자

사용 된 **엽니다 &lt;장치&gt; 이미지** c + + 프로젝트에서 장치 이미지를 열려면 대화 상자. 현재 리소스 (현재 리소스의 일부인 이미지)의 기존 장치 이미지를 나열 합니다. 포함 된 속성은:

|속성|설명|
|---|---|
|**현재 이미지**|리소스에 포함 된 이미지를 나열 합니다. 열려는 이미지 유형을 선택 합니다.|

## <a name="to-create-a-new-icon-or-cursor"></a>새 아이콘 또는 커서를 만들려면

1. [리소스 뷰](../windows/resource-view-window.md),.rc 파일을 마우스 오른쪽 단추로 클릭 한 다음 선택 **삽입 리소스** 바로 가기 메뉴에서. (단추로 cursor와 같은.rc 파일에서 기존 이미지 리소스가 이미 있는 경우는 **커서** 선택한 폴더 **커서 삽입** 바로 가기 메뉴에서.)

   > [!NOTE]
   > 프로젝트에 .rc 파일이 아직 없는 경우 [새 리소스 스크립트 파일 만들기](../windows/how-to-create-a-resource-script-file.md)를 참조하세요.

1. 에 [리소스 삽입 대화 상자](../windows/add-resource-dialog-box.md)를 선택 **아이콘** 또는 **커서** 선택한 **새**합니다. 아이콘에 대 한이 작업은 32 × 32를 16 색 아이콘을 사용 하 여 아이콘 리소스를 만듭니다. 커서의 경우 32 × 32 단색 (2-색) 이미지가 생성 됩니다.

   더하기 기호 (**+**)에서 이미지 리소스 형식을 옆에 표시 되는 **삽입 리소스** 대화 상자, 즉 모음 템플릿을 사용할 수 있습니다. 템플릿의 목록을 확장 하는 템플릿을 선택 하 고 선택 하려면 더하기 기호 **새로 만들기**합니다.

## <a name="requirements"></a>요구 사항

없음

## <a name="see-also"></a>참고 항목

[아이콘 및 커서: 디스플레이 장치용 이미지 리소스](../windows/icons-and-cursors-image-resources-for-display-devices-image-editor-for-icons.md)<br/>
[액셀러레이터 키](../windows/accelerator-keys-image-editor-for-icons.md)<br/>
[아이콘 및 커서: 디스플레이 장치용 이미지 리소스](../windows/icons-and-cursors-image-resources-for-display-devices-image-editor-for-icons.md)<br/>
[이미지 메뉴](../windows/image-menu-image-editor-for-icons.md)<br/>
[아이콘에 대한 이미지 편집기](../windows/image-editor-for-icons.md)<br/>
