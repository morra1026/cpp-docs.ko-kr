---
title: 보기 및 대화 상자 (c + +)에 ActiveX 컨트롤을 추가 합니다.
ms.date: 11/04/2016
f1_keywords:
- vc.controls.activex
- vc.editors.dialog.insertActiveXControls
helpviewer_keywords:
- dialog boxes [C++], adding ActiveX controls
- ActiveX controls [C++], adding to dialog boxes
- Insert ActiveX Control dialog box [C++]
- controls [C++], editing properties
- ActiveX controls [C++], properties
ms.assetid: e1c2e3ae-e1b0-40d3-9766-623007073856
ms.openlocfilehash: 139407ec1d4e1bfad6bb06854dc24b86ce7014e8
ms.sourcegitcommit: b488462a6e035131121e6f32d8f3b108cc798b5e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55293613"
---
# <a name="viewing-and-adding-activex-controls-to-a-dialog-box-c"></a>보기 및 대화 상자 (c + +)에 ActiveX 컨트롤을 추가 합니다.

Visual Studio에서는 ActiveX 컨트롤을 대화 상자에 삽입할 수 있습니다.

합니다 **ActiveX 컨트롤 삽입** 대화 상자를 사용 하면 사용 하는 동안 대화 상자에 ActiveX 컨트롤을 삽입 하는 [대화 상자 편집기](../windows/dialog-editor.md)합니다. 이 대화 상자에는 다음 속성이 포함 됩니다.

|속성|설명|
|---|---|
|**ActiveX 컨트롤**|Activex 컨트롤의 목록을 표시합니다. 이 대화 상자에서 컨트롤을 삽입 하는 래퍼 클래스를 생성 하지 않습니다. 래퍼 클래스를 해야 하는 경우 사용 하 여 [클래스 뷰](/visualstudio/ide/viewing-the-structure-of-code) 만들려면 (자세한 내용은 참조 하십시오 [클래스를 추가](../ide/adding-a-class-visual-cpp.md)). 이 대화 상자에서 Activex 컨트롤을 없으면 공급 업체의 지침에 따라 컨트롤을 설치 하십시오.|
|**Path**|ActiveX 컨트롤은 찾을 수 있는 파일이 표시 됩니다.|

컨트롤을 배치할 수 있습니다는 **도구 상자** 창에 쉽게 액세스할 수 있도록 합니다. 자세한 내용은 [도구 상자](/visualstudio/ide/reference/)를 참조하세요.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대한 내용은 [데스크톱 앱에 대한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)를 참조하세요. 관리되는 앱의 전역화 및 지역화 리소스에 대한 내용은 [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index)을 참조하세요.

## <a name="to-see-the-activex-controls-you-have-available"></a>사용 가능한 ActiveX 컨트롤을 확인하려면

1. 대화 상자 편집기에서 대화 상자를 엽니다.

1. 대화 상자의 본문에서 아무 곳 이나 마우스 오른쪽 단추로 클릭 합니다.

1. 바로 가기 메뉴에서 선택 **ActiveX 컨트롤 삽입**합니다.

   합니다 **ActiveX 컨트롤 삽입** 시스템에서 모든 ActiveX 컨트롤을 보여 주는 대화 상자가 나타납니다. 대화 상자 아래쪽에 ActiveX 컨트롤 파일 경로가 표시됩니다.

## <a name="to-add-an-activex-control-to-a-dialog-box"></a>대화 상자에 ActiveX 컨트롤을 추가하려면

1. 에 **ActiveX 컨트롤 삽입** 대화 상자, 대화 상자에 추가 하 고 선택 하려는 컨트롤을 선택 **확인**합니다.

   컨트롤이 대화 상자에 표시되고, 이 대화 상자에서 컨트롤을 편집하거나 다른 컨트롤처럼 컨트롤용 처리기를 만들 수 있습니다.

   > [!NOTE]
   > ActiveX 컨트롤을 [도구 상자 창](/visualstudio/ide/reference/toolbox)에 추가할 수 있습니다.

   > [!CAUTION]
   > 시스템에 일부 ActiveX 컨트롤을 배포하지 못할 수 있습니다. 컨트롤을 설치한 소프트웨어에 대한 사용권 계약을 참조하거나 소프트웨어 회사에 문의하세요.

   컨트롤을 배치할 수 있습니다는 **도구 상자** 창에 쉽게 액세스할 수 있도록 합니다. 자세한 내용은 [도구 상자](/visualstudio/ide/reference/toolbox)를 참조하세요.

## <a name="to-edit-properties-for-an-activex-control"></a>ActiveX 컨트롤에 대 한 속성을 편집 하려면

개별 공급 업체에서 제공 하는 ActiveX 컨트롤 속성 및 특성 자체와 함께 가져올 수 있습니다. ActiveX 컨트롤에 대 한 속성에 표시 되는 **속성** 창입니다. ActiveX 컨트롤의 작성자가 만든 모든 속성 페이지에 표시 됩니다는 또한 합니다 **속성 페이지** 대화 상자 (보려는 합니다 **속성 페이지** 특정 ActiveX 컨트롤을 클릭 합니다  **속성 페이지** 단추를 [속성 창](/visualstudio/ide/reference/properties-window)).

ActiveX 컨트롤의 일부로 제공 되는 속성 시트에 따라 ActiveX 컨트롤에 대 한 속성 페이지에서 다양 한 탭 표시 됩니다.

> [!NOTE]
> 속성 페이지를 사용 하 여 ActiveX 컨트롤을 편집 하려면 다음 절차에 적용 됩니다. 또한 이동 하 고 새 ActiveX 속성을 편집할 수 있습니다 **속성** 창입니다.

1. 선택 된 **ActiveX** 제어 합니다.

1. 에 **뷰** 메뉴에서 **속성 페이지** 속성을 확인 합니다.

1. 속성 페이지에서 필요에 따라 변경 합니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고 항목

[대화 상자의 컨트롤](../windows/controls-in-dialog-boxes.md)<br/>
[MFC ActiveX 컨트롤](../mfc/mfc-activex-controls.md)<br/>
[ActiveX 컨트롤 컨테이너](../mfc/activex-control-containers.md)<br/>
[ActiveX 컨트롤 보기 및 대화 상자에 추가](../windows/viewing-and-adding-activex-controls-to-a-dialog-box.md)<br/>
[도구 상자, 대화 상자 편집기 탭](../windows/dialog-editor-tab-toolbox.md)<br/>
[리소스 파일](../windows/resource-files-visual-studio.md)<br/>
