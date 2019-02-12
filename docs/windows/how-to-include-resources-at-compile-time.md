---
title: '방법: (C + +) 컴파일 타임에 리소스 포함'
ms.date: 11/04/2016
f1_keywords:
- vs.resvw.resource.including
- vc.resvw.resource.including
- vc.editors.resourceincludes
helpviewer_keywords:
- comments [C++], compiled files
- resources [C++], including at compile time
- projects [C++], including resources
- '#include directive'
- include directive (#include)
- Resource Includes dialog box [C++]
- rc files [C++], changing storage
- symbol header files [C++], changing
- .rc files [C++], changing storage
- symbol header files [C++], read-only
- symbols [C++], symbol header files
- directories [C++], specifying include paths for resources
- include files [C++], specifying for resources
- resources [C++], including in projects
- symbols [C++], finding
- resources [C++], searching for symbols
ms.assetid: 357e93c2-0a29-42f9-806f-882f688b8924
ms.openlocfilehash: 8df5a8ee6583b1e9f5c50a428b69babb0d56961b
ms.sourcegitcommit: f4be868c0d1d78e550fba105d4d3c993743a1f4b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56152380"
---
# <a name="how-to-include-resources-at-compile-time-c"></a>방법: (C + +) 컴파일 타임에 리소스 포함

일반적으로 쉽고 편리 하 게 하나의 리소스 스크립트 (.rc) 파일에서 모든 리소스의 기본 배열을 사용 하는 것이 것입니다. 그러나 하면 리소스를 추가할 수 다른 파일의 현재 프로젝트 컴파일 타임에 나열 합니다 **컴파일 시간 지시문** 상자에 **리소스 내용** 대화 상자.

다음과 같은 여러 가지 이유로 주 .rc 파일이 아닌 다른 파일에 리소스를 배치합니다.

- .Rc 파일을 저장할 때 삭제 되지 않는 리소스 문에 주석을 추가 합니다.

   리소스 편집기에서.rc 읽지 직접 또는 `resource.h` 파일입니다. 리소스 컴파일러는 리소스 편집기에서 사용되는 이러한 파일을 .aps 파일로 컴파일합니다. 이 파일은 컴파일 단계이며 기호화된 데이터만 저장합니다. 일반적인 컴파일 프로세스를 따라 없는 (예: 주석) 기호화 된 정보에는 컴파일 프로세스 중 삭제 됩니다. .Rc 파일을.aps 파일이.rc 파일과 동기화 gets, 때마다 다시 생성 됩니다 (예를 들어 저장 하면 리소스 편집기에서 파일을 덮어씁니다.rc 및 `resource.h` 파일). 리소스 자체의 모든 변경 내용은 .rc 파일에 통합된 상태로 유지되지만 주석은 .rc 파일을 덮어쓰면 항상 손실됩니다.

- 이미 개발 되 고 테스트 하는 리소스를 포함할 필요 하지 않습니다 추가 수정 합니다. 포함 되었지만.rc 확장명이 없는 모든 파일 없습니다 일 리소스 편집기에서 편집할 수 있습니다.

- 여러 다른 프로젝트에서 사용 중인 또는 소스 코드 버전 제어 시스템의 일부분이 며 따라서 수정 모든 프로젝트에 적용 됩니다 중앙 위치에 있어야 하는 리소스를 포함 합니다.

- 사용자 지정 형식인 리소스(예: RCDATA 리소스)를 포함하기 위해서입니다. RCDATA 리소스에는 특별한 요구 사항이 있을 수 있습니다. 예를 들어 nameID 필드의 값으로 식을 사용할 수 없습니다. 자세한 내용은 Windows SDK 설명서를 참조하세요.

섹션에서는 이러한 조건 중 하나라도 충족 하는 기존.rc 파일에 있는 경우 하나에 섹션을 배치 해야 하거나 별도.rc 파일 및 사용 하 여 프로젝트에 포함 된 **리소스 내용** 대화 상자. 합니다 *Projectname*.rc2 파일을 새 프로젝트의 \res 하위 디렉터리에 생성이 용도로 사용 됩니다.

사용할 수는 **리소스 내용** 환경의 기본 작업 수정할에서 프로젝트.rc 파일 및 모든 리소스를 모두 저장 하는 c + + 프로젝트의 대화 상자 [기호](../windows/symbols-resource-identifiers.md) Resource.h에 있습니다.

열려는 합니다 **리소스 내용** 대화 상자에서 마우스 오른쪽 단추로 클릭.rc 파일 [리소스 뷰](../windows/resource-view-window.md), 선택한 **리소스 내용** 바로 가기 메뉴에서. 이 대화 상자에 다음 속성이 있습니다.

|속성|설명|
|---|---|
|**기호 헤더 파일**|리소스 파일에 대한 기호 정의가 저장되는 헤더 파일의 이름을 변경할 수 있습니다. 자세한 내용은 [기호 헤더 파일의 이름 변경](../windows/changing-the-names-of-symbol-header-files.md)합니다.|
|**읽기 전용 기호 지시문**|편집 세션 중 수정 하지 않아야 하는 기호를 포함 하는 헤더 파일을 포함할 수 있습니다. 예를 들어 여러 프로젝트 간에 공유되는 기호 파일을 포함할 수 있습니다. MFC .h 파일을 포함할 수도 있습니다. 자세한 내용은 [비롯 한 공유 (읽기 전용) 또는 계산 된 기호](../windows/including-shared-read-only-or-calculated-symbols.md)합니다.|
|**컴파일 시간 지시문**|만들어지고 주 리소스 파일에 리소스에서 개별적으로 편집 되는 리소스 파일을 포함할 수 있습니다 (예: 해당 지시문 조건에 따라), 컴파일 시간 지시문을 포함 하거나 사용자 지정 형식에서 리소스를 포함할 수도 있습니다. 사용할 수도 있습니다는 **컴파일 시간 지시문 상자** 표준 MFC 리소스 파일을 포함 합니다. 자세한 내용은 [컴파일 타임에 리소스 포함](../windows/how-to-include-resources-at-compile-time.md)합니다.|

> [!NOTE]
> 이러한 텍스트 상자에 항목으로 표시.rc 파일에 나타나는 `TEXTINCLUDE 1`, `TEXTINCLUDE 2`, 및 `TEXTINCLUDE 3` 각각. 자세한 내용은 참조 하세요. [TN035: Visual c + +를 사용 하 여 여러 리소스 파일과 헤더 파일을 사용 하 여](../mfc/tn035-using-multiple-resource-files-and-header-files-with-visual-cpp.md)입니다.

사용 하 여 리소스 파일에 변경 내용을 적용 하 고 나면 합니다 **리소스 내용** .rc 파일을 닫은 다음 다시 변경 내용을 적용 하려면 필요한 대화 상자.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) .NET Framework Developer's Guide에 있습니다.

## <a name="to-include-resources-in-your-project-at-compile-time"></a>컴파일 시간에 프로젝트에 리소스를 포함하려면

1. 고유한 파일 이름으로 리소스 스크립트 파일에 리소스를 배치합니다. 사용 하지 마세요 *projectname*.rc 파일 이름을 주 리소스 스크립트 파일에 사용 되 고 있으므로.

1. .Rc 파일을 마우스 오른쪽 단추로 클릭 (에서 [리소스 뷰](../windows/resource-view-window.md))를 선택 하 고 **리소스 내용** 바로 가기 메뉴에서.

1. 에 **컴파일 시간 지시문** 상자에서 추가 합니다 [#include](../preprocessor/hash-include-directive-c-cpp.md) 컴파일러 지시문을 개발 환경에서 주 리소스 파일에 새 리소스 파일을 포함 합니다.

   이런 식으로 포함된 파일의 리소스는 컴파일 시간에 실행 파일의 일부가 됩니다. 프로젝트의 주.rc 파일에서 작업할 때 직접 편집 하거나 수정 하기 위해 사용할 수 없습니다. 개별적으로 포함 된.rc 파일을 엽니다. 포함 되었지만.rc 확장명이 없는 모든 파일은 리소스 편집기에서 편집할 수 없습니다.

## <a name="to-specify-include-directories-for-a-specific-resource-rc-file"></a>지정 하는 특정 리소스 (.rc 파일)에 대 한 디렉터리를 포함 합니다.

1. 솔루션 탐색기에서.rc 파일을 마우스 오른쪽 단추로 누르고 **속성** 바로 가기 메뉴에서.

1. 에 **속성 페이지** 대화 상자를 선택 합니다 **리소스** 왼쪽된 창에서 노드 추가 포함 디렉터리를 지정 합니다는 **추가 포함 디렉터리**속성입니다.

## <a name="to-find-symbols-in-resources"></a>리소스에서 기호를 찾으려면

1. **편집할** 메뉴 선택 **기호 찾기**합니다.

1. 에 [기호 찾기 대화 상자](/visualstudio/ide/go-to)를 **찾을 내용** 상자, 드롭 다운 목록에서 이전에 검색 문자열을 선택 하거나 (예: ID_ACCEL1) 찾으려는 액셀러레이터 키를 입력 합니다.

   > [!TIP]
   > 사용 하도록 [정규식](/visualstudio/ide/using-regular-expressions-in-visual-studio) 검색을 사용 해야 합니다는 [파일에서에서 찾기 명령](/visualstudio/ide/reference/find-command) 에서 합니다 **편집** 대신 메뉴는 **기호 찾기**명령입니다. 정규식을 사용 하도록 설정 하려면 해야는 **사용: Regular Expressions** 확인란을 선택 합니다 [찾기 대화 상자](/visualstudio/ide/finding-and-replacing-text)합니다. 오른쪽의 오른쪽 화살표 단추를 선택할 수 있습니다 합니다 **찾을 내용** 정규 검색 식의 목록을 표시 하려면 상자입니다. 검색 텍스트로 대체 식을이 목록에서를 선택 하면 합니다 **찾을 내용** 상자입니다.

1. 중 하나를 선택 합니다 **찾을** 옵션입니다.

1. **다음 찾기**를 선택합니다.

> [!NOTE]
> 문자열, 액셀러레이터 또는 이진 리소스에서 기호를 검색할 수 없습니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고자료

[리소스 파일](../windows/resource-files-visual-studio.md)<br/>
[리소스 편집기](../windows/resource-editors.md)<br/>
[기호: 리소스 식별자](../windows/symbols-resource-identifiers.md)<br/>