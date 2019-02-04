---
title: 256 색상표 사용(아이콘에 대한 이미지 편집기)
ms.date: 11/04/2016
helpviewer_keywords:
- 256-color palette
- cursors [C++], color
- colors [C++], icons
- colors [C++], cursors
- icons, color
- colors [C++], icons and cursors
- color palettes, 256-color
- palettes, 256-color
ms.assetid: 2738089b-4fd3-4c45-96ae-6a15e4c6b780
ms.openlocfilehash: 4e2f2c9ce58799756137bb47db42e52c97a43d39
ms.sourcegitcommit: e98671a4f741b69d6277da02e6b4c9b1fd3c0ae5
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/04/2019
ms.locfileid: "55702897"
---
# <a name="using-the-256-color-palette-image-editor-for-icons"></a>256 색상표 사용(아이콘에 대한 이미지 편집기)

사용 하 여 **이미지** 편집기, 아이콘 및 커서 선택할 256 색 색상표를 사용 하 여 크기가 큰 (64 × 64) 될 수 있습니다. 리소스를 만든 후 장치 이미지 스타일을 선택 합니다.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대한 내용은 [데스크톱 앱에 대한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)를 참조하세요. 관리되는 앱의 전역화 및 지역화 리소스에 대한 내용은 [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index)을 참조하세요.

## <a name="to-create-a-256-color-icon-or-cursor"></a>256 색 아이콘이 나 커서를 만들려면

1. [리소스 뷰](../windows/resource-view-window.md),.rc 파일을 마우스 오른쪽 단추로 클릭 한 다음 선택 **삽입 리소스** 바로 가기 메뉴에서. (단추로 cursor와 같은.rc 파일에서 기존 이미지 리소스가 이미 있는 경우는 **커서** 선택한 폴더 **커서 삽입** 바로 가기 메뉴에서.)

   > [!NOTE]
   > 프로젝트에 .rc 파일이 아직 없는 경우 [새 리소스 스크립트 파일 만들기](../windows/how-to-create-a-resource-script-file.md)를 참조하세요.

1. 에 [리소스 삽입 대화 상자](../windows/add-resource-dialog-box.md)를 선택 **아이콘** 또는 **커서** 선택한 **새**합니다.

1. 에 **이미지** 메뉴에서 **새 장치 이미지**합니다.

1. 원하는 256 색 이미지 스타일을 선택 합니다.

## <a name="to-choose-a-color-from-the-256-color-palette-for-large-icons"></a>큰 아이콘에 대 한 256 색상표에서 색을 선택 하려면

그릴을 선택 하 여 256 색상표에서 색을 선택 해야 합니다 **색** 색상표에는 [색 창](../windows/colors-window-image-editor-for-icons.md)합니다.

1. 큰 아이콘 또는 커서를 선택 하거나 새 큰 아이콘 또는 커서를 만듭니다.

1. 에 표시 된 256 색에서 색을 선택 합니다 **색** 색상표에는 **색** 창입니다.

   선택한 색은 현재 색으로 표시 됩니다는 **색** 색상표에는 **색** 창입니다.

   > [!NOTE]
   > 256 컬러 이미지에 사용 되는 초기 색상표를 반환한 색상표와 일치 하는 `CreateHalftonePalette` Windows API입니다. Windows shell을 위한 모든 아이콘 색상표 인식 하는 동안 깜박임을 방지 하기 위해이 색상표를 사용 해야 합니다.

## <a name="requirements"></a>요구 사항

없음

## <a name="see-also"></a>참고 항목

[액셀러레이터 키](../windows/accelerator-keys-image-editor-for-icons.md)<br/>
[아이콘 및 커서: 디스플레이 장치용 이미지 리소스](../windows/icons-and-cursors-image-resources-for-display-devices-image-editor-for-icons.md)
