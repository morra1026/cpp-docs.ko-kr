---
title: 대화 상자 (c + +) 만들기
ms.date: 11/04/2016
f1_keywords:
- vc.editors.dialog
helpviewer_keywords:
- dialog boxes [C++], creating
- Dialog Editor [C++], creating dialog boxes
- modal dialog boxes [C++], logon screens
- logon screens
ms.assetid: 303de801-c4f8-42e1-b622-353f6423f688
ms.openlocfilehash: 928432000fb9a6347433b78b224e15f07ce810d2
ms.sourcegitcommit: 52c05e10b503e834c443ef11e7ca1987e332f876
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/05/2019
ms.locfileid: "55742650"
---
# <a name="creating-a-dialog-box-c"></a>대화 상자 (c + +) 만들기

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대한 내용은 [데스크톱 앱에 대한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)를 참조하세요. 관리되는 앱의 전역화 및 지역화 리소스에 대한 내용은 [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index)을 참조하세요.

## <a name="to-create-a-new-dialog-box"></a>새 대화 상자를 만들려면

1. [리소스 뷰](../windows/resource-view-window.md),.rc 파일을 마우스 오른쪽 단추로 클릭 한 다음 선택 **리소스 추가** 바로 가기 메뉴에서.

   > [!NOTE]
   > 프로젝트에 .rc 파일이 아직 없는 경우 [새 리소스 스크립트 파일 만들기](../windows/how-to-create-a-resource-script-file.md)를 참조하세요.

1. 에 **리소스 추가** 대화 상자에서 **대화** 에 **리소스 종류** 목록에서 선택한 **새로 만들기**합니다.

   더하기 기호 (**+**) 옆에 표시 되는 **대화** 리소스 유형에 의미는 대화 상자 템플릿을 사용할 수 있습니다. 템플릿의 목록을 확장 하는 템플릿을 선택 하 고 선택 하려면 더하기 기호 **새로 만들기**합니다.

   새 대화 상자에서 열립니다는 **대화 상자** 편집기입니다.

   할 수도 있습니다 [대화 상자 편집기에서 편집을 위해 기존 대화 상자를 열어](../windows/viewing-and-editing-resources-in-a-resource-editor.md)합니다.

## <a name="to-create-a-dialog-box-that-a-user-cant-exit"></a>사용자가 종료할 수 없는 대화 상자를 만들려면

사용자가 종료할 수 없는 런타임 대화 상자를 만들 수 있습니다. 이 종류의 대화 상자는 로그온에 유용하며, 애플리케이션 또는 문서를 잠그는 데에도 유용합니다.

1. 대화 상자의 **속성** 창에서 **시스템 메뉴** 속성을 **false**로 설정합니다.

   이 설정은 대화 상자의 시스템 메뉴를 사용 하지 않도록 설정 하 고 **닫기** 단추입니다.

1. 대화 상자 폼에서 **취소** 및 **확인** 단추를 삭제합니다.

   런타임 시 사용자는 이러한 특징이 있는 모달 대화 상자를 종료할 수 없습니다.

테스트 대화 상자는 검색 될 때 대화 상자의 이러한 종류의 테스트를 사용 하려면 **Esc** 눌러져 있습니다. (**Esc** VK_ESCAPE 가상 키라고도 하는 것이 라고도 합니다.) 런타임에 동작 대화 상자는 디자인 하는 방법에 관계 없이 키를 눌러 테스트 모드를 종료할 수 있습니다 **Esc**합니다.

> [!NOTE]
> MFC 응용 프로그램에 대 한 사용자가 종료할 수 없습니다. 대화 상자를 만들려면 재정의 해야의 기본 동작 `OnOK` 하 고 `OnCancel` 키를 눌러 대화 상자를 닫을 여전히 수 연결된 단추를 삭제 하는 경우에 하기 때문에  **입력** 나 **Esc**합니다.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index)합니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고 항목

[방법: 리소스 만들기](../windows/how-to-create-a-resource.md)<br/>
[리소스 파일](../windows/resource-files-visual-studio.md)<br/>
[대화 상자 편집기](../windows/dialog-editor.md)