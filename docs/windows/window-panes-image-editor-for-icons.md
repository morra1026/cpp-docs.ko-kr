---
title: 창(아이콘에 대한 이미지 편집기)
ms.date: 11/04/2016
f1_keywords:
- vc.editors.bitmap
- vc.editors.icon
helpviewer_keywords:
- graphics editor [C++]
- Image editor [C++], panes
- Image editor [C++], magnification
- grids, pixel
- pixel grid, Image editor
- Image editor [C++], pixel grid
- Image editor [C++], grid settings
- grid settings, Image editor
ms.assetid: d66ea5b3-e2e2-4fc4-aa99-f50022cc690e
ms.openlocfilehash: 72b7cf056147cdbd216d861f0e710da423951c5a
ms.sourcegitcommit: efcc8c97570ddf7631570226c700e8f6ebb6c7be
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/01/2019
ms.locfileid: "55560311"
---
# <a name="window-panes-image-editor-for-icons"></a>창(아이콘에 대한 이미지 편집기)

합니다 **이미지 편집기** 창은 일반적으로 분할 막대로 구분 된 두 창에 이미지를 표시 합니다. 그 중 하나는 실제 크기 및 다른 확대 됩니다 (기본 확대 비율을이 6). 이러한 두 창의 뷰를 자동으로 업데이트 됩니다: 하나의 창에서 수행한 변경 내용에 다른 바로 표시 됩니다. 두 개의 창이 사용 하면 쉽게 더 크게 보려면 이미지를 수 있습니다 각 픽셀을 구분 하 고 있는, 동시에 이미지의 실제 크기 보기에서 작업의 효과 관찰의 작업할 수 있습니다.

필요한 만큼 많은 공간을 사용 하는 왼쪽된 창 (의 최대 절반를 **이미지** 창) 이미지를 기본값인 1:1 비율로 표시 합니다. 오른쪽 창 확대/축소 된 이미지 (기본적으로 6:1 비율로)를 표시 합니다. 사용 하 여 각 창에서 배율을 변경할 수 있습니다는 **확대** 도구를 [이미지 편집기 도구 모음](../windows/toolbar-image-editor-for-icons.md) 또는 액셀러레이터 키를 사용 하 여 합니다.

더 작은 창을 확대할 수 있습니다 합니다 **이미지 편집기** 창 두 창을 사용 하 여 큰 이미지의 다른 영역을 표시 합니다. 선택 하 고 창 내에서 선택 합니다.

분할 막대에 포인터를 놓고 오른쪽 또는 왼쪽 분할 막대를 이동 하 여 창의 상대적 크기를 변경할 수 있습니다. 분할 막대 하나의 창에서 작업 하려는 경우 어느 쪽으로 이동할 수 있습니다.

경우는 **이미지 편집기** 창은 4 비율로 확대 이상, 이미지의 개별 픽셀을 구분 하는 픽셀 모눈을 표시할 수 있습니다.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대한 내용은 [데스크톱 앱에 대한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)를 참조하세요. 관리되는 앱의 전역화 및 지역화 리소스에 대한 내용은 [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index)을 참조하세요.

## <a name="to-change-the-magnification-factor"></a>확대 비율 변경

기본적으로 **이미지** 실제 크기로 왼쪽된 창에서 보기를 표시 하는 편집기 및 6에서 오른쪽 창에서 보기 시간 실제 크기입니다. 확대 비율 (작업 영역 맨 아래에 상태 표시줄에 표시 됨)에 이미지의 실제 크기와 표시 크기 간의 비율입니다. 기본 비율을 6 이며 범위는 1부터 10 까지입니다.

1. 선택 된 **이미지 편집기** 창 확대 비율을 변경 합니다.

1. 에 [이미지 편집기 도구 모음](../windows/toolbar-image-editor-for-icons.md), 오른쪽의 화살표를 선택 합니다 [확대 도구](../windows/toolbar-image-editor-for-icons.md) 하위 메뉴에서 확대 비율을 선택 하 고: **1 X**하십시오 **2 X**, **6 X**, 또는 **8 X**합니다.

   > [!NOTE]
   > 에 나열 되지 않은 확대 비율을 선택 하는 **Magnify** 도구, 액셀러레이터 키를 사용 합니다.

## <a name="to-display-or-hide-the-pixel-grid"></a>표시 하거나 숨기려면 픽셀 모눈

모든 **이미지 편집기** 4 이상인 확대 비율을 사용 하 여 창 이미지의 개별 픽셀을 구분 하는 모눈을 표시할 수 있습니다.

1. 에 **이미지** 메뉴에서 **모눈 설정**합니다.

1. 선택 된 **픽셀 모눈** 모눈을 표시 하거나 표를 숨기려면 확인란의 선택을 취소 하려면 확인란 합니다.

> [!TIP]
> 도구 모음 단추 위로 커서를 올려 놓으면 도구 설명이 표시 됩니다. 이러한 팁 각 단추의 기능을 식별할 수 있습니다.

## <a name="requirements"></a>요구 사항

없음

## <a name="see-also"></a>참고 항목

[액셀러레이터 키](../windows/accelerator-keys-image-editor-for-icons.md)<br/>
[아이콘에 대한 이미지 편집기](../windows/image-editor-for-icons.md)