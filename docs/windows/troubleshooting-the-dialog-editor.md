---
title: (C + +) 대화 상자 편집기 문제 해결
ms.date: 11/04/2016
helpviewer_keywords:
- controls [C++], troubleshooting
- Dialog Editor [C++], troubleshooting
- dialog boxes [C++], troubleshooting
- InitCommonControls
- RichEdit 1.0 control
- rich edit controls [C++], RichEdit 1.0
ms.assetid: 21882868-5ac4-4a41-a4a6-eaaa059402ea
ms.openlocfilehash: fe0fe704b5c17d0db4e3419f29d21f0e60bc4211
ms.sourcegitcommit: 5270117dbecc4c49bca0cf10b927bae3c9930038
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/31/2019
ms.locfileid: "55484957"
---
# <a name="troubleshooting-the-dialog-editor-c"></a>(C + +) 대화 상자 편집기 문제 해결

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대한 내용은 [데스크톱 앱에 대한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)를 참조하세요. 관리되는 앱의 전역화 및 지역화 리소스에 대한 내용은 [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index)을 참조하세요.

다음은 몇 가지 문제는 c + +에서 작업할 때 알고 있어야 **대화 상자** 편집기:

## <a name="adding-controls-to-a-dialog-causes-the-dialog-to-no-longer-function"></a>대화 상자에 컨트롤을 추가 하면 더 이상 함수

공용 컨트롤 또는 서식 있는 편집 컨트롤을 대화 상자를 추가한 후 대화 상자를 테스트할 때나 자체 대화 상자에 나타나지는 표시 되지 않습니다.

### <a name="example-of-the-problem"></a>문제 예

1. Windows 응용 프로그램 (콘솔 앱)을 만든 하므로 응용 프로그램 설정을 수정 Win32 프로젝트를 만듭니다.

1. [리소스 뷰](../windows/resource-view-window.md),.rc 파일을 두 번 클릭 합니다.

1. 대화 상자 옵션에서 두 번 클릭 합니다 **에 대 한** 상자입니다.

1. 추가 된 **IP 주소 컨트롤** 대화 상자.

1. 저장 하 고 **모두 다시 빌드**합니다.

1. 프로그램을 실행 합니다.

1. 대화 상자에서 **도움말** 메뉴에서 클릭 합니다 **에 대 한** 명령; 없는 대화 상자가 표시 됩니다.

### <a name="the-cause"></a>원인

현재는 **대화 상자** rich edit 컨트롤을 대화 상자에 끌어다 놓으면 다음과 같은 일반적인 컨트롤 또는 때 편집기 프로젝트에 자동으로 코드 추가 하지 않습니다. 도 Visual Studio 제공 오류 또는 경고가 발생이 문제가 발생 합니다. 를 해결 하려면 컨트롤에 대 한 코드를 수동으로 추가 합니다.

||||
|-|-|-|
|슬라이더 컨트롤|트리 컨트롤|날짜 시간 선택|
|스핀 컨트롤|탭 컨트롤|Month Calendar|
|진행률 컨트롤|애니메이션 컨트롤|IP 주소 컨트롤|
|바로 가기 키|Rich Edit 컨트롤|확장 된 콤보 상자|
|목록 컨트롤|Rich Edit 2.0 컨트롤|사용자 지정 컨트롤|

### <a name="fix-for-common-controls"></a>공용 컨트롤에 대 한 수정

대화 상자에서 공용 컨트롤을 사용 하려면 호출 [InitCommonControlsEx](/windows/desktop/api/commctrl/nf-commctrl-initcommoncontrolsex) 또는 `AFXInitCommonControls` 대화 상자를 만들어야 합니다.

### <a name="fix-for-richedit-controls"></a>RichEdit 컨트롤에 대 한 수정

호출 해야 `LoadLibrary` rich edit 컨트롤에 대 한 합니다. 자세한 내용은 [Rich Edit 컨트롤](/windows/desktop/Controls/about-rich-edit-controls) Windows sdk에서 및 [서식 있는 편집 컨트롤의 개요](../mfc/overview-of-the-rich-edit-control.md)합니다.

### <a name="requirements"></a>요구 사항

Win32

## <a name="using-the-richedit-10-control-with-mfc"></a>MFC에 RichEdit 1.0 컨트롤 사용

RichEdit 컨트롤을 사용 하려면 먼저 불러와야 [AfxInitRichEdit2](../mfc/reference/application-information-and-management.md#afxinitrichedit2) RichEdit 2.0 컨트롤 (RICHED20 로드 하려면. DLL)를 호출 하거나 [AfxInitRichEdit](../mfc/reference/application-information-and-management.md#afxinitrichedit) 이전에 RichEdit 1.0 컨트롤 (RICHED32 로드 하려면. DLL)입니다.

현재 사용할 수 있습니다 [CRichEditCtrl](../mfc/reference/cricheditctrl-class.md) 이전 RichEdit 1.0 컨트롤을 사용 하 여 클래스 이지만 `CRichEditCtrl` RichEdit 2.0 제어를 지원 하도록 디자인 되었습니다. RichEdit 1.0 및 2.0 RichEdit 유사한 이기 때문에 대부분의 메서드가 작동 합니다. 그러나 일부의 차이점이 1.0 및 2.0 컨트롤 간의 몇 가지 방법을 제대로 작동 하지 않을 수 있습니다 하거나 전혀 작동 하지 않음 note 합니다.

### <a name="requirements"></a>요구 사항

MFC

## <a name="see-also"></a>참고 항목

[대화 상자 편집기](../windows/dialog-editor.md)