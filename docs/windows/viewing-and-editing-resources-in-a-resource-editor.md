---
title: 리소스 편집기 (c + +)에서 리소스 보기 및 편집
ms.date: 11/04/2016
f1_keywords:
- vs.resourceview
- vc.resvw.resource.previewing
- vs.resvw.resource.previewing
helpviewer_keywords:
- resources [C++], viewing
- layouts, previewing resource
- resource editors [C++], viewing resources
- .rc files [C++], viewing resources
- resources [C++], editing
- properties [C++], resources
- resources [C++], properties
ms.assetid: ba8bdc07-3f60-43c7-aa5c-d5dd11f0966e
ms.openlocfilehash: 02ab58d37f3f188c3d65740b218cb9b2ac799714
ms.sourcegitcommit: 52c05e10b503e834c443ef11e7ca1987e332f876
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/05/2019
ms.locfileid: "55742663"
---
# <a name="viewing-and-editing-resources-in-a-resource-editor-c"></a>리소스 편집기 (c + +)에서 리소스 보기 및 편집

각 리소스 종류에는 **리소스** 리소스 유형에 특정 한 편집기입니다. 다시 정렬의 크기를 조정 하거나 컨트롤 및 기능을 추가 합니다. 그렇지 않으면 연결된 된 편집기를 사용 하 여 리소스의 기능을 수정할 수 있습니다. 리소스를 편집할 수도 있습니다 [텍스트 형식](../windows/how-to-open-a-resource-script-file-in-text-format.md) 하 고 [이진 형식](../windows/opening-a-resource-for-binary-editing.md)합니다.

일부 리소스 종류는 개별 파일을 가져오고; 다양 한 방식에서으로 사용할 수 있습니다. 여기에 비트맵, 아이콘, 커서, 도구 모음 및 html 파일이 포함 됩니다. 이러한 리소스에 파일 이름이 고 [리소스 식별자](../windows/symbols-resource-identifiers.md)합니다. 다른 Win32 프로젝트에 있는 문자열 테이블 대화 상자, 메뉴 등 존재 리소스 스크립트 (.rc) 파일 또는 리소스 템플릿 (.rct) 파일의 일부로 합니다.

> [!NOTE]
> 리소스의 속성 [속성 창을 사용 하 여 수정할 수 있습니다](../windows/changing-the-properties-of-a-resource.md)합니다.

## <a name="win32-resources"></a>Win32 리소스

Win32 리소스에 액세스할 수 있습니다 합니다 [리소스 뷰](../windows/resource-view-window.md) 창입니다.

### <a name="to-view-a-win32-resource-in-a-resource-editor"></a>리소스 편집기에서 Win32 리소스를 보려면

1. 선택 **리소스 뷰** 에서 합니다 **보기** 메뉴.

1. 경우는 **리소스 뷰** 선택 최상위 창이 아닌 합니다 **리소스 뷰** 를 맨 위로 이동 하려면 탭 합니다.

1. **리소스 뷰**를 보려는 리소스를 포함 하는 프로젝트에 대 한 폴더를 확장 합니다. 대화 상자 리소스를 보려는 경우 확장 하는 예를 들어 합니다 **대화 상자** 폴더입니다.

   > [!NOTE]
   > 프로젝트에 .rc 파일이 아직 없는 경우 [새 리소스 스크립트 파일 만들기](../windows/how-to-create-a-resource-script-file.md)를 참조하세요.

1. 예를 들어 리소스를 두 번 클릭 **IDD_ABOUTBOX**합니다.

   리소스가 해당 편집기에서 열립니다. 예를 들어, 대화 상자 리소스에서 열립니다는 **대화 상자** 편집기입니다.

   할 수도 있습니다 [프로젝트를 열지 않고도.rc (리소스 스크립트) 파일에서 리소스를 볼](../windows/how-to-open-a-resource-script-file-outside-of-a-project-standalone.md)합니다.

### <a name="to-delete-an-existing-win-32-resource"></a>기존 win32 리소스를 삭제 하려면

1. **리소스 뷰**, 리소스 종류에 대 한 노드를 확장 합니다.

2. 선택한 삭제 하려는 리소스를 마우스 오른쪽 단추로 클릭 **삭제** 바로 가기 메뉴에서.

   > [!NOTE]
   > .Rc 파일이 프로젝트 외부에서 문서 창에 열려 있는 경우 동일한 바로 가기 메뉴 명령을 사용 하 여 리소스를 삭제할 수 있습니다.

## <a name="resources-in-managed-projects"></a>관리 되는 프로젝트의 리소스

리소스를 관리 되는 프로젝트에서 리소스 스크립트 파일을 사용 하지 않으므로 열어야 **솔루션 탐색기**합니다. 관리되는 프로젝트에서 리소스 파일로 작업하려면 [이미지 편집기](../windows/image-editor-for-icons.md) 및 [바이너리 편집기](binary-editor.md) 를 사용할 수 있습니다. 편집할 관리되는 리소스는 연결된 리소스여야 합니다. Visual Studio 리소스 편집기가 포함 된 리소스 편집을 지원 하지 않습니다.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대한 내용은 [데스크톱 앱에 대한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)를 참조하세요. 관리되는 앱의 전역화 및 지역화 리소스에 대한 내용은 [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index)을 참조하세요.

### <a name="to-view-a-managed-resource-in-a-resource-editor"></a>리소스 편집기에서 관리 되는 리소스를 보려면

**솔루션 탐색기**, 예를 들어 리소스를 두 번 클릭 **Bitmap1.bmp**합니다.

   리소스가 해당 편집기에서 열립니다.

### <a name="to-delete-an-existing-managed-resource"></a>기존 관리 되는 리소스를 삭제 하려면

**솔루션 탐색기**를 선택 하 고 삭제 하려는 리소스를 마우스 오른쪽 단추로 클릭 **삭제** 바로 가기 메뉴에서.

## <a name="changing-the-properties-of-resources"></a>리소스의 속성 변경

### <a name="to-edit-the-properties-of-a-resource"></a>리소스 속성을 편집하려면

1. [리소스 뷰](../windows/resource-view-window.md)을 편집 하 고 선택 하려는 리소스를 마우스 오른쪽 단추로 클릭 **속성** 바로 가기 메뉴에서.

   > [!NOTE]
   > 프로젝트에 .rc 파일이 아직 없는 경우 [새 리소스 스크립트 파일 만들기](../windows/how-to-create-a-resource-script-file.md)를 참조하세요.

1. 에 [속성 창](/visualstudio/ide/reference/properties-window), 리소스의 속성을 변경 합니다.

### <a name="to-undo-a-change-made-to-the-properties-of-a-resource"></a>리소스의 속성에 대 한 변경을 취소 하려면

1. 리소스에 포커스를가지고 있는지 **리소스 뷰**합니다.

1. 선택할 **실행 취소** 에서 합니다 **편집** 메뉴.

## <a name="previewing-resources"></a>리소스 미리 보기

그래픽 리소스를 열지 않고 볼 수 있도록 리소스를 미리 봅니다. 리소스 식별자를 숫자로 변경 되므로 컴파일된 한 후에 미리 보기는 실행 파일에 대 한 유용 합니다. 종종 이러한 숫자 식별자는 충분 한 정보를 제공 하지 않습니다, 이후 리소스를 미리 보기 사용 하면 신속 하 게 식별할 수 있습니다.

다음 리소스 종류의 시각적 레이아웃을 미리 볼 수 있습니다.

- Bitmap

- 대화 상자

- 아이콘

- 메뉴

- Cursor

- ToolBar

Visual 미리 보기 함수 가속기, 매니페스트, 문자열 테이블 및 버전 정보 리소스에 적용 되지 않습니다.

### <a name="to-preview-resources"></a>리소스를 미리 보려면

1. [리소스 뷰](../windows/resource-view-window.md) 또는 문서 창에 예를 들어, 리소스 선택 **IDD_ABOUTBOX**합니다.

   > [!NOTE]
   > 프로젝트에 .rc 파일이 아직 없는 경우 [새 리소스 스크립트 파일 만들기](../windows/how-to-create-a-resource-script-file.md)를 참조하세요.

1. 에 [속성 창](/visualstudio/ide/reference/properties-window)를 선택 합니다 **속성 페이지** 단추입니다.

   \- 또는 -

   에 **뷰** 메뉴에서 **속성 페이지**합니다.

   합니다 **속성 페이지** 열리고 리소스에 대 한 해당 리소스의 미리 보기를 표시 합니다. 사용할 수 있습니다 합니다 **위로** 및 **아래로** 에서 트리를 탐색 하려면 화살표 키를 제어할 **리소스 뷰** 나 문서 창을 합니다. 합니다 **속성 페이지** 개방 하며에 포커스가 생기 며 미리 볼 수 있는 모든 리소스를 표시 합니다.

> [!NOTE]
> 리소스를 미리 보려면 Win32 필요 합니다.

## <a name="requirements"></a>요구 사항

없음

## <a name="see-also"></a>참고자료

[방법: 프로젝트 외부에서 리소스 스크립트 파일 열기(독립 실행형)](../windows/how-to-open-a-resource-script-file-outside-of-a-project-standalone.md)<br/>
[리소스 편집기](../windows/resource-editors.md)