---
title: 바이너리 편집기 (c + +)
ms.date: 02/14/2019
f1_keywords:
- vc.editors.binary.F1
- vc.editors.binary
helpviewer_keywords:
- editors, Binary
- resources [C++], editing
- resource editors [C++], Binary editor
- Binary editor
- binary data, editing
- resources [C++], opening for binary editing
- binary data
- hexadecimal bytes in binary data
- strings [C++], searching for
- file searches [C++]
- binary data, finding
- ASCII characters, finding in binary data
- custom resources [C++]
- data resources [C++]
- resources [C++], creating
ms.assetid: 2483c48b-1252-4dbc-826b-82e6c1a0e9cb
ms.openlocfilehash: 2a3ff3d89c809f57ea3ddbd70d5664fc8d13cec4
ms.sourcegitcommit: 470de1337035dd33682d935b4b6c6d8b1bdb0bbb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56320824"
---
# <a name="binary-editor-c"></a>바이너리 편집기 (c + +)

> [!WARNING]
> 합니다 **바이너리 편집기** 를 Express 버전에서는 사용할 수 없습니다.

바이너리 편집기를 사용하면 16진수 또는 ASCII 형식으로 바이너리 수준에서 리소스를 편집할 수 있습니다. 또한 [찾기 명령](/visualstudio/ide/reference/find-command) 을 사용하여 ASCII 문자열 또는 16진수 바이트를 검색할 수도 있습니다. 사용 해야 합니다 **이진** 편집기 보기 또는 부 버전을 확인 해야 하는 경우에 변경 사용자 지정 리소스 또는 리소스 형식이 Visual Studio 환경에서 지원 되지 않습니다.

여는 **바이너리 편집기**를 먼저 선택 **파일** > **새로 만들기** > **파일** 주 메뉴에서 선택 합니다 파일을 편집 하 고 다음 드롭다운 화살표를 선택 합니다 **열려** 단추를 선택한 **연결** > **바이너리 편집기**합니다.

> [!CAUTION]
> 바이너리 편집기에서 대화 상자, 이미지 또는 메뉴와 같은 리소스를 편집하는 것은 위험합니다. 잘못된 편집으로 리소스가 손상되어 해당 네이티브 편집기에서 읽지 못하게 될 수 있습니다.

![Binary Editor](../mfc/media/vcbinaryeditor2.gif "vcBinaryEditor2")<br/>
바이너리 편집기에 표시되는 대화 상자의 이진 데이터

바이너리 편집기에는 특정 ASCII 값만 표시됩니다(0x20 ~ 0x7E). 확장 문자는 바이너리 편집기의 ASCII 값 섹션(오른쪽 패널)에 마침표로 표시됩니다. "인쇄 가능" 문자는 ASCII 값 32 ~ 126입니다.

> [!TIP]
> 사용 하는 동안 합니다 **이진** 리소스별 명령의 바로 가기 메뉴를 표시할 단추로 편집기 경우가 많습니다. 사용할 수 있는 명령은 커서가 가리키는 내용에 따라 달라집니다. 예를 들어을 가리키는 동안 클릭 하면 합니다 **이진** 선택한 16 진수 값을 사용 하 여 편집기 바로 가기 메뉴에 표시 합니다 **잘라내기**, **복사**, 및 **붙여넣기**  명령입니다.

## <a name="how-to"></a>방법

합니다 **이진** 편집기가 있습니다.

### <a name="to-open-a-windows-desktop-resource-for-binary-editing"></a>이진 편집을 위해 Windows 데스크톱 리소스를 열려면

1. [리소스 뷰](../windows/resource-view-window.md)에서 편집할 특정 리소스 파일을 선택합니다.

1. 리소스를 마우스 오른쪽 단추로 클릭하고 바로 가기 메뉴에서 **이진 데이터 열기** 를 클릭합니다.

   > [!NOTE]
   > 사용 하는 경우는 [리소스 뷰](../windows/resource-view-window.md) 는 Visual Studio는 인식 되지 않는 형식의 (예: RCDATA 또는 사용자 지정 리소스)에 리소스를 사용 하 여 리소스를 열려면 창에서 자동으로 열릴 합니다 **이진** 편집기.

### <a name="to-open-a-managed-resource-for-binary-editing"></a>이진 편집을 위해 관리되는 리소스를 열려면

1. **솔루션 탐색기**, 편집할 특정 리소스 파일을 선택 합니다.

1. 리소스를 마우스 오른쪽 단추로 클릭하고 바로 가기 메뉴에서 **연결 프로그램** 을 선택합니다.

1. **연결 프로그램** 대화 상자에서 **바이너리 편집기**를 선택합니다.

   > [!NOTE]
   > 관리되는 프로젝트에서 리소스 파일로 작업하려면 [이미지 편집기](../windows/image-editor-for-icons.md) 및 [바이너리 편집기](binary-editor.md) 를 사용할 수 있습니다. 편집할 관리되는 리소스는 연결된 리소스여야 합니다. Visual Studio 리소스 편집기에서는 포함된 리소스를 편집할 수 없습니다.

> [!NOTE]
> 사용 하려는 경우는 **이진** 편집기 이미 다른 편집기 창에서 편집 중인 리소스에 먼저 다른 편집기 창을 닫아야 합니다.

### <a name="to-edit-a-resource"></a>리소스를 편집하려면

1. 편집 하려는 바이트를 선택 합니다.

   합니다 **탭** 키의 16 진수 및 ASCII 섹션 간에 포커스를 이동 합니다 **이진** 편집기입니다. 사용할 수는 **Page Up** 하 고 **Page Down** 한 번에 하나의 리소스 화면을 통해 이동 하는 키입니다.

1. 새 값을 입력합니다.

   값이 16 진수 및 ASCII 섹션 모두에서 즉시 변경 되 고 줄에서 다음 값으로 포커스가 이동 합니다.

   > [!NOTE]
   > 합니다 **이진** 편집기 변경 내용을 자동으로 적용 된 편집기를 닫을 때.

### <a name="to-find-binary-data"></a>이진 데이터를 찾으려면

ASCII 문자열 또는 16 진수 바이트를 검색할 수 있습니다. 예를 들어, "Hello"을 찾으려면 검색할 수 있습니다에 대 한 문자열 "Hello" 또는 "48 65 6C C 6F 6" (16 진수).

1. **편집** 메뉴 선택 [찾을](/visualstudio/ide/reference/find-command)합니다.

1. 에 **찾을 내용** 상자, 드롭 다운 목록에서 이전에 검색 문자열을 선택 하거나 찾으려는 데이터를 입력 합니다.

1. 중 하나를 선택 합니다 **찾을** 선택한 옵션 **다음 찾기**합니다.

### <a name="to-create-a-new-custom-or-data-resource"></a>새 사용자 지정 또는 데이터 리소스를 만들려면

프로젝트를 마우스 오른쪽 단추로 클릭 하 여 기본 리소스 스크립트 (.rc) 파일 구문을 사용 하 여 별도 파일에 다음 파일을 포함 하는 리소스를 배치 하 여 새 사용자 지정 또는 데이터 리소스를 만들 수 있습니다 **솔루션 탐색기** 클릭 **리소스 포함** 바로 가기 메뉴.

1. 사용자 지정 또는 데이터 리소스가 포함된[.rc 파일을 만듭니다](../windows/how-to-create-a-resource-script-file.md) .

   null로 끝나는 따옴표가 붙은 문자열이나 10진수, 16진수 또는 8진수 형식의 정수로 .rc 파일의 사용자 지정 데이터를 입력할 수 있습니다.

1. **솔루션 탐색기**에서 프로젝트의 .rc 파일을 마우스 오른쪽 단추로 클릭한 후 바로 가기 메뉴에서 **리소스 내용** 을 클릭합니다.

1. 에 **컴파일 시간 지시문** 상자에 입력을 `#include` 문을 사용자 지정 리소스를 포함 하는 파일의 이름을 제공 하는 합니다. 예를 들어:

    ```cpp
    #include mydata.rc
    ```

   입력한 구문 및 맞춤법이 정확한지 확인합니다. **컴파일 타임 지시문** 상자의 내용은 입력한 대로 정확하게 리소스 스크립트 파일에 삽입됩니다.

1. 선택 **확인** 변경 내용을 기록 합니다.

사용자 지정 리소스를 만드는 또 다른 방법은 사용자 지정 리소스와 같이 외부 파일을 가져오는 것입니다. 자세한 내용은 [리소스 가져오기 및 내보내기](../windows/how-to-import-and-export-resources.md)를 참조하세요.

> [!NOTE]
> 새 사용자 지정 또는 데이터 리소스를 만들려면 Win32 필요 합니다.

## <a name="requirements"></a>요구 사항

없음

## <a name="see-also"></a>참고 항목

[리소스 편집기](../windows/resource-editors.md)