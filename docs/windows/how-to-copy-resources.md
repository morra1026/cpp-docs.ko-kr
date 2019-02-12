---
title: '방법: 관리 리소스 (c + +)'
ms.date: 11/04/2016
f1_keywords:
- vc.resvw.resource.copying
- vs.resvw.resource.copying
- vc.resvw.resource.changing
- vb.xmldesigner.data
- vs.resvw.resource.importing
- vc.resvw.resource.importing
helpviewer_keywords:
- resources [C++], moving between files
- resources [C++], copying
- resource files [C++], copying or moving resources between
- resource files [C++], tiling
- .rc files [C++], copying resources between
- rc files [C++], copying resources between
- Language property [C++]
- .resx files [C++], editing
- resource files [C++], editing
- resx files [C++], editing
- resources [C++], exporting
- graphics [C++], exporting
- graphics [C++], importing
- resources [C++], importing
- bitmaps [C++], importing and exporting
- toolbars [C++], importing
- images [C++], importing
- toolbars [C++], exporting
- cursors [C++], importing and exporting
- images [C++], exporting
ms.assetid: 65f523e8-017f-4fc6-82d1-083c56d9131f
ms.openlocfilehash: e8b976f974e397b8012ebf59ede08ee64f4f7191
ms.sourcegitcommit: f4be868c0d1d78e550fba105d4d3c993743a1f4b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/12/2019
ms.locfileid: "56150794"
---
# <a name="how-to-manage-resources-c"></a>방법: 관리 리소스 (c + +)

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대한 내용은 [데스크톱 앱에 대한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)를 참조하세요. 관리되는 앱의 전역화 및 지역화 리소스에 대한 내용은 [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index)을 참조하세요.

## <a name="to-copy-resources"></a>리소스 복사

변경 하지 않고 다른 리소스 파일에서 복사할 수 하 하거나 복사 하는 동안 언어 또는 리소스의 상태를 변경할 수 있습니다.

현재 리소스 파일에 기존 리소스 또는 실행 파일에서 리소스를 쉽게 복사할 수 있습니다. 리소스를 복사 하려면 동시에 리소스를 포함 하는 두 파일을 열고 및 다른 하나의 파일에서 항목을 끌어 또는 복사 하는 두 파일 사이 붙여 넣습니다. 이 메서드는 실행 파일 (.exe)와 리소스 스크립트 (.rc) 파일 및 리소스 템플릿 (.rct) 파일에 대 한 작동합니다.

> [!NOTE]
> Visual c + + 응용 프로그램에서 사용할 수 있는 샘플 리소스 파일을 포함 합니다. 자세한 내용은 참조 하세요. [클립 아트. 일반적인 리소스](https://github.com/Microsoft/VCSamples)합니다.

끌어서 놓기 메서드를 사용 하 여 열려 있는.rc 파일 간에 [프로젝트 외부에서](../windows/how-to-open-a-resource-script-file-outside-of-a-project-standalone.md)합니다.

### <a name="to-copy-resources-between-files-using-the-drag-and-drop-method"></a>끌어서 놓기 메서드를 사용 하 여 파일 간에 리소스를 복사 하려면

1. 독립 실행형 두 리소스 파일을 엽니다 (자세한 내용은 [프로젝트 외부에서.rc 파일에서 리소스를 볼](../windows/how-to-open-a-resource-script-file-outside-of-a-project-standalone.md)). 예를 들어 열 *Source1.rc* 하 고 *Source2.rc*합니다.

1. 내 첫 번째.rc 파일을 복사 하려는 리소스를 선택 합니다. 예를 들어 *Source1.rc*를 선택 **IDD_DIALOG1**합니다.

1. 누른 합니다 **Ctrl** 키 및 두 번째.rc 파일의 리소스를 끕니다. 예를 들어 끌어 **IDD_DIALOG1** 에서 *Source1.rc* 하 *Source2.rc*합니다.

   > [!NOTE]
   > 리소스를 누르지 않고 끌기 합니다 **Ctrl** 복사 하는 것이 아니라 리소스 키를 누르면 합니다.

### <a name="to-copy-resources-using-copy-and-paste"></a>복사를 사용 하 여 리소스를 복사 및 붙여 넣으려면

1. 독립 실행형 두 리소스 파일을 엽니다 (자세한 내용은 [프로젝트 외부에서.rc 파일에서 리소스를 볼](../windows/how-to-open-a-resource-script-file-outside-of-a-project-standalone.md)). 예를 들어 *Source1.rc* 하 고 *Source2.rc*합니다.

1. 리소스를 복사 하려는 소스 파일에서 (예를 들어 *Source1.rc*), 리소스를 마우스 오른쪽 단추로 클릭 하 고 선택 **복사** 바로 가기 메뉴에서.

1. 리소스를 붙여 하려는 리소스 파일을 마우스 오른쪽 단추로 클릭 (예를 들어 *Source2.rc*). 선택할 **붙여넣기** 바로 가기 메뉴에서.

   > [!NOTE]
   > 및 삭제, 복사, 잘라내기를 끌거나 수 간의 프로젝트에서 리소스 파일에 붙여 넣습니다 (**리소스 뷰**) 및 독립 실행형.rc 파일 (문서 창에서 열기). 이전 버전의 제품에서이 수행할 수 있습니다.

   > [!NOTE]
   > 기호 이름이 나 기존 파일의 값을 사용 하 여 충돌을 방지 하려면 Visual c + + 변경 될 수 있습니다 되는 리소스의 기호 값 또는 기호 이름 및 값 새 파일에 복사 하면 됩니다.

### <a name="to-change-the-language-or-condition-of-a-resource-while-copying"></a>복사 하는 동안 언어 또는 리소스의 상태를 변경 하려면

리소스에서 복사하는 동안 언어 속성이나 조건 속성 또는 두 가지 모두를 변경할 수 있습니다.

- 리소스의 언어는 말 그대로 리소스용 언어를 식별합니다. 언어를 사용해 [FindResource](/windows/desktop/api/winbase/nf-winbase-findresourcea) 를 찾고 있는 리소스를 식별 하는 데 있습니다. 그러나 (리소스 각 언어에 대 한 텍스트 관련 없는 차이점이 있을 수 있습니다, 그리고 가속기는 일본어 자판 에서만 작동할 수 있습니다 하거나 비트맵이 중국어로 지역화 된 적절 하 게 작성 하는 예를 들어)

- 리소스의 조건은 리소스의 해당 특정 복사본이 사용되는 조건을 식별하는 정의된 기호입니다.

언어 및 리소스의 조건은 리소스의 이름 뒤에 오는 괄호 안에 표시 됩니다는 **작업 영역** 창입니다. 이 예제에서는 명명 된 리소스가 `IDD_AboutBox` 사용 하는 `Finnish` 는 해당 언어 및 조건으로 `XX33`입니다.

```cpp
IDD_AboutBox (Finnish - XX33)
```

기존 리소스를 복사 및 해당 언어 또는 조건을 변경 합니다.

1. .Rc 파일 또는 합니다 [리소스 뷰](../windows/resource-view-window.md) 창에서 복사 하려는 리소스를 마우스 오른쪽 단추로 클릭 합니다.

1. 선택할 **복사본 삽입** 바로 가기 메뉴에서.

1. 에 **리소스 복사본 삽입** 대화 상자:

   - 에 대 한 합니다 **언어** 목록 상자에서 언어를 선택 합니다.

   - 에 **조건을** 상자에서 조건을 입력 합니다.

## <a name="to-edit-managed-resource-files"></a>관리 되는 리소스 파일을 편집 하려면

관리 되는 리소스 (.resx) 파일에는 XML 파일입니다. 관리 되는 리소스 파일에서 프로젝트에 추가 되는 경우는 **새 항목 추가** 대화 상자를 **관리 되는 리소스 편집기** 기본적으로 열립니다.

## <a name="to-import-and-export-resources"></a>가져오기 및 내보내기 리소스

Visual C++에서 사용하도록 그래픽 리소스(비트맵, 아이콘, 커서 및 도구 모음), HTML 파일 및 사용자 지정 리소스를 가져올 수 있습니다. Visual C++ 프로젝트에서 동일한 형식의 파일을 개발 환경 외부에서 사용할 수 있는 별도의 파일로 내보낼 수 있습니다.

> [!NOTE]
> 액셀러레이터 키, 대화 상자 및 문자열 테이블과 같은 리소스 종류는 독립 실행형 파일 형식이 아니므로 가져오거나 내보낼 수 없습니다.

### <a name="to-import-an-individual-resource-into-your-current-resource-file"></a>현재 리소스 파일로 개별 리소스를 가져오려면

1. [리소스 뷰](../windows/resource-view-window.md), 리소스 스크립트에 대 한 노드를 마우스 오른쪽 단추로 클릭 (*.rc) 리소스를 추가 하려면 원하는 파일입니다.

1. 선택 **가져오기** 바로 가기 메뉴.

1. 비트맵(.bmp), 아이콘(.ico), 커서(.cur), Html 파일(.htm) 또는 기타 가져오려는 파일의 파일 이름을 찾아 선택합니다.

1. 선택할 **확인** 에서 선택한 파일에 리소스를 추가 하려면 **리소스** 보기.

   > [!NOTE]
   > 가져오기 프로세스는 선택한 특정 리소스 종류에 관계없이 동일한 방식으로 작동합니다. 가져온 리소스는 해당 리소스 종류에 적합한 노드에 자동으로 추가됩니다.

### <a name="to-export-a-bitmap-icon-or-cursor-as-a-separate-file-for-use-outside-of-visual-c"></a>Visual C++ 외부에서 사용하도록 비트맵, 아이콘 또는 커서를 별도의 파일로 내보내려면

1. **리소스** 보기에서 내보낼 리소스를 마우스 오른쪽 단추로 클릭 합니다.

1. 선택 **내보내기** 바로 가기 메뉴.

1. 에 **리소스 내보내기** 대화 상자에서 현재 파일 이름을 그대로 사용 하거나 새 이름을 입력 합니다.

1. 선택한 파일을 저장 하려는 폴더로 이동한 후 **내보내기**합니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고자료

[리소스 파일](../windows/resource-files-visual-studio.md)<br/>
[리소스 편집기](../windows/resource-editors.md)