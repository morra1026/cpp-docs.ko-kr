---
title: 이미지 크기 조정(아이콘에 대한 이미지 편집기)
ms.date: 11/04/2016
f1_keywords:
- vc.editors.image.editing
helpviewer_keywords:
- Image editor [C++], resizing images
- graphics [C++], resizing
- images [C++], resizing
- resizing images
- size [C++], images
- images [C++], cropping
- images [C++], extending
- Image editor [C++], cropping or extending images
- Image editor [C++], shrinking and stretching images
- images [C++], stretching
- images [C++], shrinking
- bitmaps [C++], shrinking
- bitmaps [C++], stretching
ms.assetid: d83a02c4-4dfe-4586-a0df-51a50c2ba71d
ms.openlocfilehash: d88a4cccff5b9b7b6303329782b7367cb953b13d
ms.sourcegitcommit: 5270117dbecc4c49bca0cf10b927bae3c9930038
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/31/2019
ms.locfileid: "55484970"
---
# <a name="resizing-an-image-image-editor-for-icons"></a>이미지 크기 조정(아이콘에 대한 이미지 편집기)

동작을 **이미지** 이미지 크기 조정 하는 동안 편집기 인지에 따라 달라 집니다 [선택한](../windows/selecting-an-area-of-an-image-image-editor-for-icons.md) 전체 이미지 또는의 일부입니다.

이미지의 일부만 포함 하 여 선택 하는 경우는 **이미지** 편집기 픽셀의 행 이나 열을 삭제 하 고 현재 배경색을 사용 하 여 빈된 영역을 입력 하 여 선택 영역을 축소 합니다. 또한 픽셀의 행 이나 열을 복제 하 여 선택 영역을 확장할 수 것.

전체 이미지를 포함 하 여 선택 하는 경우는 **이미지** 편집기 중 축소 및 이미지를 자릅니다 및 확장 합니다.

메커니즘은 두 가지 이미지 크기 조정에 대 한: 크기 조정 핸들 및 [속성 창](/visualstudio/ide/reference/properties-window)합니다. 이미지의 일부나 모두의 크기를 변경 하려면 크기 조정 핸들을 끌어 있습니다. 끌 수 있는 크기 조정 핸들은 실선입니다. 속이 빈 핸들을 끌 수 없습니다. 사용 된 **속성** 전체 크기를 조정 하려면 창의 이미지만, 선택된 된 부분이 아닌 합니다.

![비트맵의 핸들 크기 조정](../mfc/media/vcimageeditorsizinghandles.gif "vcImageEditorSizingHandles")<br/>
크기 조정 핸들

> [!NOTE]
> 있는 경우는 **바둑판식 모눈** 옵션을 선택 합니다 [모눈 설정 대화 상자](../windows/grid-settings-dialog-box-image-editor-for-icons.md), 다음 바둑판식 모눈에 스냅숏 크기 조정이 합니다. 경우는 **픽셀 모눈** 옵션은 (기본 설정)를 선택 하면 다음 사용 가능한 픽셀 눈금의 크기를 조정 합니다.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대한 내용은 [데스크톱 앱에 대한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)를 참조하세요. 관리되는 앱의 전역화 및 지역화 리소스에 대한 내용은 [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index)을 참조하세요.

## <a name="to-resize-an-entire-image-using-the-properties-window"></a>속성 창을 사용 하 여 전체 이미지 크기를 조정 하려면

1. 변경할 속성 이미지를 엽니다.

1. 에 **너비** 및 **높이** 상자에 [속성 창](/visualstudio/ide/reference/properties-window)를 원하는 크기를 입력 합니다.

   이미지의 크기를 증가 하는 경우는 **이미지** 편집기 오른쪽 이나 아래쪽 이미지 또는 둘 모두를 확장 하 고 새 영역을 현재 배경색으로 채웁니다. 이미지를 채우도록 확장 되지 않습니다.

   이미지의 크기를 단축 합니다 **이미지** 편집기의 오른쪽 가장자리나 아래쪽 가장자리 또는 둘 다에서 이미지를 자릅니다.

   > [!NOTE]
   > 사용할 수는 **너비** 하 고 **높이** 일부 선택 영역이 필요가 전체 이미지, 크기를 조정 하는 속성입니다.

## <a name="to-crop-or-extend-an-entire-image"></a>자르거나 전체 이미지를 확장 하려면

1. 전체 이미지를 선택 합니다.

   이미지의 일부는 현재 선택한 경우 전체 이미지를 선택 하려는, 현재 선택 영역 경계 외부에 있는 이미지 아무 곳 이나 선택 합니다.

1. 이미지에 적절 한 크기는 때까지 크기 조정 핸들을 끕니다.

일반적으로 **이미지** 편집기 자릅니다 또는 크기 조정 핸들을 이동 하 여 해당 크기를 조정할 때 이미지를 확대 합니다. 누른 채 합니다 **Shift** 크기 조정 핸들을 이동할 때 키를 **이미지** 편집기를 축소 하거나 확장 하는 이미지입니다.

## <a name="to-shrink-or-stretch-an-entire-image"></a>전체 이미지를 확장 또는 축소 하려면

1. 전체 이미지를 선택 합니다.

   현재 선택 된 이미지의 부분을 전체 이미지를 선택 하는 경우 현재 선택 영역 경계 외부에 있는 이미지 아무 곳 이나 선택 합니다.

1. 누른 합니다 **Shift** 키 및 크기 조정 핸들을 끌어 이미지의 크기가 적합 합니다.

## <a name="to-shrink-or-stretch-part-of-an-image"></a>이미지의 일부를 확장 또는 축소 하려면

1. 크기를 조정 하려면 이미지의 일부를 선택 합니다. 자세한 내용은 [이미지 영역 선택](../windows/selecting-an-area-of-an-image-image-editor-for-icons.md)합니다.

1. 선택 영역 오른쪽 크기가 될 때까지 크기 조정 핸들 중 하나를 끕니다.

## <a name="requirements"></a>요구 사항

없음

## <a name="see-also"></a>참고 항목

[액셀러레이터 키](../windows/accelerator-keys-image-editor-for-icons.md)<br/>
[그래픽 리소스 편집](../windows/editing-graphical-resources-image-editor-for-icons.md)<br/>
[아이콘에 대한 이미지 편집기](../windows/image-editor-for-icons.md)