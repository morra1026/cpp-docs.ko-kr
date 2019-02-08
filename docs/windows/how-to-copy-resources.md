---
title: '방법: 리소스 복사 (c + +)'
ms.date: 11/04/2016
f1_keywords:
- vc.resvw.resource.copying
- vs.resvw.resource.copying
- vc.resvw.resource.changing
helpviewer_keywords:
- resources [C++], moving between files
- resources [C++], copying
- resource files [C++], copying or moving resources between
- resource files [C++], tiling
- .rc files [C++], copying resources between
- rc files [C++], copying resources between
- Language property [C++]
ms.assetid: 65f523e8-017f-4fc6-82d1-083c56d9131f
ms.openlocfilehash: 772c9b905d4cb0c4e2ccab9ec51aa02860b2db32
ms.sourcegitcommit: bd637e9c39650cfd530520ea978a22fa4caa0e42
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/07/2019
ms.locfileid: "55849663"
---
# <a name="how-to-copy-resources-c"></a>방법: 리소스 복사 (c + +)

변경 하지 않고 다른 리소스 파일에서 복사할 수 하 하거나 복사 하는 동안 언어 또는 리소스의 상태를 변경할 수 있습니다.

현재 리소스 파일에 기존 리소스 또는 실행 파일에서 리소스를 쉽게 복사할 수 있습니다. 리소스를 복사 하려면 동시에 리소스를 포함 하는 두 파일을 열고 및 다른 하나의 파일에서 항목을 끌어 또는 복사 하는 두 파일 사이 붙여 넣습니다. 이 메서드는 실행 파일 (.exe)와 리소스 스크립트 (.rc) 파일 및 리소스 템플릿 (.rct) 파일에 대 한 작동합니다.

> [!NOTE]
> Visual c + + 응용 프로그램에서 사용할 수 있는 샘플 리소스 파일을 포함 합니다. 자세한 내용은 참조 하세요. [클립 아트. 일반적인 리소스](https://github.com/Microsoft/VCSamples)합니다.

끌어서 놓기 메서드를 사용 하 여 열려 있는.rc 파일 간에 [프로젝트 외부에서](../windows/how-to-open-a-resource-script-file-outside-of-a-project-standalone.md)합니다.

## <a name="to-copy-resources-between-files-using-the-drag-and-drop-method"></a>끌어서 놓기 메서드를 사용 하 여 파일 간에 리소스를 복사 하려면

1. 독립 실행형 두 리소스 파일을 엽니다 (자세한 내용은 [는.rc 파일 외부의 프로젝트에서에서 리소스 보기](../windows/how-to-open-a-resource-script-file-outside-of-a-project-standalone.md)). 예를 들어 Source1.rc 및 Source2.rc를 엽니다.

1. 내 첫 번째.rc 파일을 복사 하려는 리소스를 선택 합니다. 예를 들어 `Source1.rc`을 선택 **IDD_DIALOG1**합니다.

1. 누른 합니다 **Ctrl** 키 및 두 번째.rc 파일의 리소스를 끕니다. 예를 들어 끌어 **IDD_DIALOG1** 에서 `Source1.rc` 하려면 `Source2.rc`합니다.

   > [!NOTE]
   > 리소스를 누르지 않고 끌기 합니다 **Ctrl** 복사 하는 것이 아니라 리소스 키를 누르면 합니다.

## <a name="to-copy-resources-using-copy-and-paste"></a>복사를 사용 하 여 리소스를 복사 및 붙여 넣으려면

1. 독립 실행형 두 리소스 파일을 엽니다 (자세한 내용은 [는.rc 파일 외부의 프로젝트에서에서 리소스 보기](../windows/how-to-open-a-resource-script-file-outside-of-a-project-standalone.md)). 예를 들어 Source1.rc 및 Source2.rc를 합니다.

1. 리소스를 복사 하려는 소스 파일에서 (예를 들어 `Source1.rc`), 리소스를 마우스 오른쪽 단추로 클릭 하 고 선택 **복사** 바로 가기 메뉴에서.

1. 리소스를 붙여 하려는 리소스 파일을 마우스 오른쪽 단추로 클릭 (예를 들어 `Source2.rc`). 선택할 **붙여넣기** 바로 가기 메뉴에서.

   > [!NOTE]
   > 및 삭제, 복사, 잘라내기를 끌거나 수 간의 프로젝트에서 리소스 파일에 붙여 넣습니다 (**리소스 뷰**) 및 독립 실행형.rc 파일 (문서 창에서 열기). 이전 버전의 제품에서이 수행할 수 있습니다.

   > [!NOTE]
   > 기호 이름이 나 기존 파일의 값을 사용 하 여 충돌을 방지 하려면 Visual c + + 변경 될 수 있습니다 되는 리소스의 기호 값 또는 기호 이름 및 값 새 파일에 복사 하면 됩니다.

## <a name="to-change-the-language-or-condition-of-a-resource-while-copying-c"></a>(C + +)를 복사 하는 동안 언어 또는 리소스의 상태를 변경 하려면

리소스에서 복사하는 동안 언어 속성이나 조건 속성 또는 두 가지 모두를 변경할 수 있습니다.

- 리소스의 언어는 말 그대로 리소스용 언어를 식별합니다. 언어를 사용해 [FindResource](/windows/desktop/api/winbase/nf-winbase-findresourcea) 를 찾고 있는 리소스를 식별 하는 데 있습니다. 그러나 (리소스 각 언어에 대 한 텍스트 관련 없는 차이점이 있을 수 있습니다, 그리고 가속기는 일본어 자판 에서만 작동할 수 있습니다 하거나 비트맵이 중국어로 지역화 된 적절 하 게 작성 하는 예를 들어)

- 리소스의 조건은 리소스의 해당 특정 복사본이 사용되는 조건을 식별하는 정의된 기호입니다.

리소스의 언어와 조건은 작업 영역 창에서 리소스 이름 뒤에 오는 괄호 안에 표시됩니다. 이 예제에서는 IDD_AboutBox 라는 리소스가 핀란드어를 사용 하는 해당 언어로 및 조건이 XX33입니다.

```cpp
IDD_AboutBox (Finnish - XX33)
```

### <a name="to-copy-an-existing-resource-and-change-its-language-or-condition"></a>기존 리소스를 복사하고 해당 언어 또는 조건을 변경하려면

1. .Rc 파일 또는 합니다 [리소스 뷰](../windows/resource-view-window.md) 창에서 복사 하려는 리소스를 마우스 오른쪽 단추로 클릭 합니다.

1. 선택할 **복사본 삽입** 바로 가기 메뉴에서.

1. 에 **리소스 복사본 삽입** 대화 상자:

   - 에 대 한 합니다 **언어** 목록 상자에서 언어를 선택 합니다.

   - 에 **조건을** 상자에서 조건을 입력 합니다.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대한 내용은 [데스크톱 앱에 대한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)를 참조하세요. 관리되는 앱의 전역화 및 지역화 리소스에 대한 내용은 [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index)을 참조하세요.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고자료

[리소스 파일](../windows/resource-files-visual-studio.md)<br/>
[리소스 편집기](../windows/resource-editors.md)<br/>
[방법: 프로젝트 외부에서 리소스 스크립트 파일 열기(독립 실행형)](../windows/how-to-open-a-resource-script-file-outside-of-a-project-standalone.md)<br/>
