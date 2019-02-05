---
title: 버전 정보 편집기 (c + +)
ms.date: 11/04/2016
f1_keywords:
- vc.editors.version.F1
- vc.editors.version
helpviewer_keywords:
- Version Information editor [C++], about Version Information editor
- editors, Version Information
- resource editors [C++], Version Information editor
- version information resources [C++]
- resources [C++], editing version information
- languages, version information
- New Version Info Block
- blocks, adding
- resources [C++], adding version information
- version information, adding for languages
- blocks, deleting
- version information, deleting blocks
- resources [C++], deleting version information
- VerQueryValue
- version information, accessing from within programs
- GetFileVersionInfo
- version information
ms.assetid: 772e6f19-f765-4cec-9521-0ad3eeb99f9b
ms.openlocfilehash: 94afb429af6eb1b0d570a444f49145a31c2fec1f
ms.sourcegitcommit: 52c05e10b503e834c443ef11e7ca1987e332f876
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/05/2019
ms.locfileid: "55742676"
---
# <a name="version-information-editor-c"></a>버전 정보 편집기 (c + +)

버전 정보는 회사 및 제품 ID, 제품 릴리스 번호, 저작권 및 상표 알림 등으로 이루어져 있습니다. 사용 하 여 합니다 **버전 정보** 편집기를 만들고 버전 정보 리소스에 저장 되어 있는이 데이터를 유지 합니다. 버전 정보 리소스는 응용 프로그램에 필요 하지 않은 이지만 응용 프로그램을 식별 하는 정보를 수집 하기에 유용한 장소입니다. 버전 정보는 설치 API에도 사용됩니다.

버전 정보 리소스에는 하나의 상위 블록과 하나 이상의 하위 블록이 있습니다. 위쪽에는 단일 고정 정보 블록이 있고, 아래쪽에는 하나 이상의 버전 정보 블록(다른 언어 및/또는 문자 집합에 대한 정보 블록)이 있습니다. 위쪽 블록에는 편집 가능한 숫자 상자와 선택 가능한 드롭다운 목록이 모두 있습니다. 하위 블록에는 편집 가능한 텍스트 상자만 있습니다.

> [!NOTE]
> Windows 표준은 VS_VERSION_INFO라고 하는 하나의 버전 리소스만 포함합니다.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대한 내용은 [데스크톱 앱에 대한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)를 참조하세요. 관리되는 앱의 전역화 및 지역화 리소스에 대한 내용은 [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index)을 참조하세요.

합니다 **버전 정보** 편집기가 있습니다.

## <a name="to-edit-a-string-in-a-version-information-resource"></a>버전 정보 리소스의 문자열을 편집하려면

편집 하려면 해당 항목을 다시 선택 하려면 항목을 한 번을 선택 합니다. 변경에 직접 합니다 **버전 정보** 테이블 또는 합니다 [속성 창](/visualstudio/ide/reference/properties-window)합니다. 변경 내용은 두 위치에 모두 반영됩니다.

   > [!NOTE]
   > 편집 하는 경우는 `FILEFLAGS` 키를 **버전 정보** 편집기를 보면 설정할 수 없습니다는 **디버그**를 **개인 빌드**, 또는 **특수 빌드** 속성 (에 **속성** 창).rc 파일에 대 한 합니다.

   - **버전 정보** 편집기 설정을 **디버그** 속성을 `#ifdef` 에 따라 리소스 스크립트는 `_DEBUG` 빌드 플래그.

   - 경우는 `Private Build` 키에는 **값** 에서 설정를 **버전 정보** 테이블에 해당 **개인 빌드** 속성 (에 **속성**  창)에 대 한 합니다 `FILEFLAGS` 키는 **True**합니다. **값** 이 비어 있으면 속성이 **False**가 됩니다. 마찬가지로 **Special Build** 키 (에 **버전 정보** 테이블)에 연결 됩니다는 **특수 빌드** 속성에 대 한를 `FILEFLAGS` 키.

클릭 하 여 문자열 블록의 정보 시퀀스를 정렬할 수 있습니다 합니다 **키** 또는 **값** 열 머리글입니다. 이들 머리글은 정보를 선택한 시퀀스로 자동으로 다시 정렬합니다.

## <a name="to-add-version-information-for-another-language-new-version-info-block"></a>다른 언어 (새 버전 정보 블록)에 대 한 버전 정보를 추가 하려면

1. [리소스 뷰](../windows/resource-view-window.md)에서 버전 정보 리소스를 두 번 클릭하여 이를 엽니다.

   > [!NOTE]
   > 프로젝트에 .rc 파일이 아직 없는 경우 [새 리소스 스크립트 파일 만들기](../windows/how-to-create-a-resource-script-file.md)를 참조하세요.

1. 버전 정보 테이블 내에서 마우스 오른쪽 단추를 클릭하고 바로 가기 메뉴에서 **새 버전 정보 블록** 을 선택합니다.

   이 명령은 현재 버전 정보 리소스에 추가 정보 블록을 추가하고 [속성 창](/visualstudio/ide/reference/properties-window)에서 해당 속성을 엽니다.

1. **속성** 창에서 새 블록에 적절한 언어 및 문자 집합을 선택합니다.

## <a name="to-delete-a-version-information-block"></a>버전 정보 블록을 삭제하려면

1. [리소스 뷰](../windows/resource-view-window.md)에서 해당 아이콘을 두 번 클릭하여 버전 정보 리소스를 엽니다.

   > [!NOTE]
   > 프로젝트에 .rc 파일이 아직 없는 경우 [새 리소스 스크립트 파일 만들기](../windows/how-to-create-a-resource-script-file.md)를 참조하세요.

1. 삭제하려는 블록 헤더를 마우스 오른쪽 단추로 클릭한 후 바로 가기 메뉴에서 **버전 정보 블록 삭제** 를 선택합니다.

   이 명령은 선택한 헤더를 삭제 하 고 나머지 버전 정보를 그대로 둡니다. 동작을 취소할 수 없습니다.

## <a name="to-access-version-information-from-within-your-program"></a>프로그램 내에서 버전 정보에 액세스하려면

프로그램 내에서 버전 정보에 액세스하려는 경우 [GetFileVersionInfo](/windows/desktop/api/winver/nf-winver-getfileversioninfoa) 함수 및 [VerQueryValue](/windows/desktop/api/winver/nf-winver-verqueryvaluea) 함수를 사용합니다.

   > [!NOTE]
   > 사용 하는 동안 합니다 **버전 정보** 편집기를 마우스 오른쪽 단추로 클릭 수 대부분 리소스별 명령의 바로 가기 메뉴를 표시 합니다. 예를 들어 블록 헤더 항목을 가리키는 동안을 선택 하면 바로 가기 메뉴에 표시 합니다 **새 버전 블록 정보** 하 고 **버전 블록 정보 삭제** 명령입니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고자료

[리소스 편집기](../windows/resource-editors.md)<br/>
[메뉴 및 기타 리소스](https://msdn.microsoft.com/library/windows/desktop/ms632583.aspx)<br/>
[버전 정보(Windows)](https://msdn.microsoft.com/library/windows/desktop/ms646981.aspx)
