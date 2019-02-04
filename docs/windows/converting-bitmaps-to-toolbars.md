---
title: 비트맵을 도구 모음 (c + +)으로 변환
ms.date: 11/04/2016
f1_keywords:
- vc.editors.newtoolbarresource
helpviewer_keywords:
- bitmaps [C++], converting to toolbars
- Toolbar editor [C++], converting bitmaps
- toolbars [C++], converting bitmaps
- New Toolbar Resource dialog box [C++]
ms.assetid: 971c181b-40f5-44be-843d-677a7c235667
ms.openlocfilehash: 31b684ff72e970a6b09748b3925564b0b372d339
ms.sourcegitcommit: e98671a4f741b69d6277da02e6b4c9b1fd3c0ae5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55702702"
---
# <a name="converting-bitmaps-to-toolbars-c"></a>비트맵을 도구 모음 (c + +)으로 변환

비트맵을 변환 하 여 c + + 프로젝트에서 새 도구 모음을 만들 수 있습니다. 비트맵에서 그래픽 도구 모음 단추 이미지를 변환합니다. 일반적으로 비트맵 각 단추에 대 한 하나의 이미지를 사용 하 여 단일 비트맵에 여러 단추 이미지를 포함합니다. 모든 크기를 수 있는 이미지 기본값인 16 픽셀 너비 및 이미지의 높이입니다. 단추 이미지의 크기를 지정할 수 있습니다 합니다 **새 도구 모음 리소스** 선택 하면 대화 상자 **도구 모음 편집기** 에서 합니다 **이미지** 이미지 편집기의 메뉴.

합니다 **새 도구 모음 리소스** 대화 상자를 사용 하면 c + + 프로젝트의 도구 모음 리소스를 추가 하는 단추의 높이 너비를 지정할 수 있습니다. 기본값은 16 × 15 픽셀입니다.

도구 모음을 만드는 데 사용 되는 비트맵은 2048의 최대 너비입니다. 설정한 경우 합니다 **단추 너비** 단추 4 개를 하나만 사용할 수 있습니다, 512입니다. 513에 너비를 설정 하는 경우만 세 개의 단추가 있습니다.

대화 상자에 다음 속성이 있습니다.

|속성|설명|
|---|---|
|**Button Width**|도구 모음 리소스 비트맵 리소스를 변환 하는 도구 모음 단추에 대 한 너비를 입력할 공간을 제공 합니다. 이미지 너비와 높이가 지정 된 자르고 색 표준 도구 모음 색 (16 색)을 사용 하도록 조정 됩니다.|
|**단추의 높이**|도구 모음 리소스 비트맵 리소스를 변환 하는 도구 모음 단추에 대 한 높이 입력할 공간을 제공 합니다. 이미지 너비와 높이가 지정 된 자르고 색 표준 도구 모음 색 (16 색)을 사용 하도록 조정 됩니다.|

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대한 내용은 [데스크톱 앱에 대한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)를 참조하세요. 관리되는 앱의 전역화 및 지역화 리소스에 대한 내용은 [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index)을 참조하세요.

## <a name="to-convert-bitmaps-to-a-toolbar"></a>비트맵을 도구 모음을 변환 하려면

1. 기존 비트맵 리소스를 엽니다는 [이미지 편집기](../windows/image-editor-for-icons.md)합니다. (.Rc 파일을 마우스 오른쪽 단추로 클릭 비트맵.rc 파일에 있지 않은 경우, 선택 **가져오기** 바로 가기 메뉴에서.rc 파일을 추가 하려는 비트맵을 이동한 다음 선택 **오픈**.)

1. **이미지** 메뉴 선택 **도구 모음 편집기**합니다.

   합니다 **새 도구 모음 리소스** 대화 상자가 나타납니다. 비트맵에 맞게 아이콘 이미지의 높이 너비를 변경할 수 있습니다. 도구 모음 편집기에서 도구 모음 이미지가 표시 됩니다.

1. 변환이 완료 명령을 변경 **ID** 사용 하 여 단추를 [속성 창](/visualstudio/ide/reference/properties-window)합니다. 새 입력 **ID** 누르거나는 **ID** 드롭 다운 목록에서.

   > [!TIP]
   > 합니다 **속성** 창 제목 표시줄에 압정 단추를 포함 합니다. 이 단추를 선택 하면 사용 하거나 사용 하지 않도록 설정 **자동 숨기기** 창에 대 한 합니다. 각 속성 창을 다시 열 필요가 없는 모든 도구 모음 단추 속성을 통해 신속 하 게 전환, 전환 **자동 숨기기** 해제 하므로 **속성** 창이 고정 합니다.

사용 하 여 새 도구 모음에서 단추 명령 Id를 변경할 수도 있습니다는 [속성 창](/visualstudio/ide/reference/properties-window)합니다. 새 도구 모음 편집에 대 한 자세한 내용은 [만들기, 이동 및 편집 도구 모음 단추](../windows/creating-moving-and-editing-toolbar-buttons.md)합니다.

## <a name="requirements"></a>요구 사항

MFC 또는 ATL

## <a name="see-also"></a>참고 항목

[새 도구 모음 만들기](../windows/creating-new-toolbars.md)<br/>
[도구 모음 편집기](../windows/toolbar-editor.md)<br/>
[도구 모음 단추 속성](../windows/toolbar-button-properties.md)<br/>
