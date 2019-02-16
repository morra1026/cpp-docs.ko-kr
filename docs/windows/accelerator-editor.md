---
title: 액셀러레이터 키 편집기 (c + +)
ms.date: 02/14/2019
f1_keywords:
- vc.editors.accelerator.F1
- vc.editors.accelerator
helpviewer_keywords:
- accelerator tables [C++], editing
- tables [C++], accelerator key
- accelerator keys [C++]
- resource editors [C++], Accelerator editor
- keyboard shortcuts [C++], Accelerator editor
- accelerator properties
- properties [C++], accelerator properties
- Type property
- Key property
- Modifier property
- VIRTKEY
- Key property
- ID property
- accelerator tables [C++], editing
- keyboard shortcuts [C++], editing in an accelerator table
- searching, in accelarator tables
- accelerator tables [C++], finding entries
- accelerator tables [C++], adding entries
- New Accelerator command
- accelerator tables [C++], deleting entries
- keyboard shortcuts [C++], deleting entry from accelerator table
- accelerator tables [C++], copying entries
- rc files [C++], moving an accelerator table entry
- .rc files [C++], moving accelerator table entries
- accelerator tables [C++], moving entries
- keyboard shortcuts [C++], property changing
- accelerator tables [C++], changing properties
ms.assetid: 013c30b6-5d61-4f1c-acef-8bd15bed7060
ms.openlocfilehash: 90ef142336cf88c5e40f78f6cc651b2bb35a0f6c
ms.sourcegitcommit: 470de1337035dd33682d935b4b6c6d8b1bdb0bbb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56320642"
---
# <a name="accelerator-editor-c"></a>액셀러레이터 키 편집기 (c + +)

액셀러레이터 키 테이블은 연관 된 명령 식별자 및 액셀러레이터 키 (바로 가기 키 라고도 함)의 목록을 포함 하는 c + + Windows 리소스입니다. 프로그램에는 액셀러레이터 키 테이블이 두 개 이상 있을 수 있습니다.

일반적으로 액셀러레이터 키는 메뉴 또는 도구 모음에서도 사용할 수 있는 프로그램 명령에 대한 바로 가기 키로 사용됩니다. 그러나 연결된 사용자 인터페이스 개체가 없는 명령에 대한 키 조합을 정의하는 데 액셀러레이터 키 테이블을 사용할 수 있습니다.

[클래스 뷰](/visualstudio/ide/viewing-the-structure-of-code) 를 사용하여 액셀러레이터 키 명령을 코드에 연결할 수 있습니다.

미리 정의 된 액셀러레이터 키의 목록을 참조 하세요 [미리 정의 된 액셀러레이터 키](../windows/predefined-accelerator-keys.md)합니다.

   > [!TIP]
   > 사용 하는 동안 합니다 **가속기** 자주 사용 되는 명령의 바로 가기 메뉴를 표시할 단추로 편집기입니다. 사용할 수 있는 명령은 포인터가 가리키는 내용에 따라 달라집니다.

   > [!NOTE]
   > Windows에서는 빈 액셀러레이터 키 테이블을 만들 수 없습니다. 항목이 없는 액셀러레이터 키 테이블을 만들 경우 해당 테이블을 저장할 때 테이블이 자동으로 삭제됩니다.

## <a name="accelerator-properties"></a>액셀러레이터 키 속성

액셀러레이터 키 속성을 설정할 수 있습니다 합니다 [속성 창](/visualstudio/ide/reference/properties-window) 언제 든 지 합니다. 사용할 수도 있습니다는 **가속기** 액셀러레이터 키 테이블에서 액셀러레이터 키 속성을 수정 하는 편집기입니다. 사용 하 여 변경 합니다 **속성** 창 또는 **가속기** 편집기는 동일한 결과 얻은: 편집 액셀러레이터 키 테이블에 바로 반영 됩니다.

### <a name="id-property"></a>ID 속성

합니다 **ID** 프로그램 코드에서 각 액셀러레이터 키 테이블 항목을 참조 하는 속성입니다. 이 항목에는 프로그램의 액셀러레이터 키 또는 키 조합을 누를 때 받을 명령 값입니다. 메뉴 항목 동일 액셀러레이터 키를 확인, 하 게 해당 Id 동일 (액셀러레이터 키 테이블의 ID 메뉴 리소스에 대 한 ID와 동일).

속성은 세 가지 각 액셀러레이터 ID에 대 한:는 **한정자** 속성을 **키** 속성 및 **형식** 속성입니다.

#### <a name="modifier-property"></a>Modifier 속성

합니다 **한정자** 속성 컨트롤 액셀러레이터 키 조합을 설정 합니다.

> [!NOTE]
> 에 **속성** 창에서이 속성은 세 가지 개별 나타납니다 **부울** 속성을 모두 제어할 수 있습니다 독립적으로: **Alt**하십시오 **Ctrl**, 및 **Shift**합니다.

다음은 사용할 수 있는 항목에 대 한 합니다 **한정자** 액셀러레이터 키 테이블의 속성:

   |값|Description|
   |-----------|-----------------|
   |**없음**|만 누르면 합니다 **키** 값입니다. 이 값은 가장 효과적으로 사용 026 통해 ASCII/ANSI 값 001로 해석 되는 ^ A-^ Z (**Ctrl + A** 를 통해 **Ctrl + Z**).|
   |**Alt**|눌러야 합니다 **Alt** 하기 전에 키를 **키** 값입니다.|
   |**Ctrl**|눌러야 합니다 **Ctrl** 하기 전에 키를 **키** 값입니다. ASCII 형식으로 유효 하지 않습니다.|
   |**Shift**|눌러야 합니다 **Shift** 하기 전에 키를 **키** 값입니다.|
   |**Ctrl+Alt**|눌러야 합니다 **Ctrl** 키와 **Alt** 하기 전에 키를 **키** 값. ASCII 형식으로 유효 하지 않습니다.|
   |**Ctrl+Shift**|눌러야 합니다 **Ctrl** 키와 **Shift** 하기 전에 키를 **키** 값. ASCII 형식으로 유효 하지 않습니다.|
   |**Alt+Shift**|눌러야 합니다 **Alt** 키 및 **Shift** 하기 전에 키를 **키** 값입니다. ASCII 형식으로 유효 하지 않습니다.|
   |**Ctrl+Alt+Shift**|눌러야 **Ctrl**를 **Alt**, 및 **Shift** 전에 **키** 값입니다. ASCII 형식으로 유효 하지 않습니다.|

#### <a name="key-property"></a>키 속성

합니다 **키** 액셀러레이터로 사용할 실제 키를 설정 하는 속성입니다.

다음은 사용할 수 있는 항목에 대 한 합니다 **키** 액셀러레이터 키 테이블의 속성:

   |값|설명|
   |-----------|-----------------|
   |0과 10 진수 형식에서 255 사이의 정수입니다.|값을 값 ASCII 또는 ANSI로 다음과 같이 처리 됩니다 있는지 여부를 결정 합니다.<br/><br/>-자리 숫자는 항상 ASCII 또는 ANSI 값이 아닌 해당 키로 해석 됩니다.<br/>-1부터 26 앞에 0을 값으로 해석 됩니다 ^ A-^ Z 영문자와 함께 누른 경우 문자의 ASCII 값을 나타내는 **Ctrl** 키를 누르고.<br/>27부터 32 까지의 값은 항상 3 자리 10 진수 값부터 032 027로 해석 됩니다.<br/>-앞에 0 또는 ANSI 값으로는 해석 되지 않는에서 033에서 255 사이의 값입니다.|
   |단일 키보드 문자입니다.|A-Z를 대문자 또는 숫자는 0-9 ASCII 또는 가상 키 값 수 만 다른 문자가 ASCII입니다.|
   |A-Z 범위의 단일 키보드 문자 (대문자)를 앞에 캐럿 (^) (예를 들어 ^ C).|이 옵션으로 눌린 키의 ASCII 값을 입력 합니다 **Ctrl** 키를 누르고 있습니다.|
   |모든 유효한 가상 키 식별자입니다.|액셀러레이터 키 테이블의 드롭 다운 키 상자에는 표준 가상 키 식별자의 목록을 포함합니다.|

> [!NOTE]
> ASCII 값을 입력 하는 경우 한정자 속성 옵션이 제한 됩니다. 사용 하기 위해 사용할 수 있는 유일한 컨트롤 키가 합니다 **Alt** 키입니다.

> [!TIP]
> 액셀러레이터 키를 정의 하는 또 다른 방법은 또는 액셀러레이터 키 테이블에서 여러 항목을 마우스 오른쪽 단추로 클릭을 선택 하는 것 **다음 입력 된 키** 바로 가기 메뉴에서 한 다음 키보드의 키 또는 키 조합 중 하나를 누릅니다. 합니다 **다음 키 입력** 명령에서 제공 됩니다. 합니다 **편집** 메뉴.

#### <a name="type-property"></a>Type 속성

합니다 **형식** 속성은 액셀러레이터 키 ID와 연결 된 바로 가기 키 조합을 ASCII/ANSI 키 값을 또는 가상 키 (VIRTKEY) 조합으로 해석할지 결정 합니다.

- 경우는 **형식** 속성이 ASCII를 **한정자** 속성 수만 있습니다 `None` 또는 `Alt`를 사용 하는 액셀러레이터 키를 가질 수 있는 **Ctrl** (키 지정 된 키 앞에 `^`).

- 경우는 **형식** 속성은 VIRTKEY를 조합 `Modifier` 및 `Key` 값이 잘못 되었습니다.

> [!NOTE]
> 액셀러레이터 키 테이블에 값을 입력 하 고 값이 ASCII/ANSI 간단히 클릭으로 처리 하려는 경우는 **형식** 드롭다운 목록에서에서 선택 ASCII 테이블의 항목에 대 한 합니다. 그러나 사용 하는 경우는 **다음 입력 된 키** 명령 (**편집** 메뉴) 지정 하는 `Key`를 변경 해야 합니다는 **형식** ascii VIRTKEY속성*하기 전에* 입력을 `Key` 코드입니다.

## <a name="accelerator-tables"></a>액셀러레이터 키 테이블

C + + 프로젝트에서 직접 사용 하 여 현재 위치에서 편집 액셀러레이터 키 테이블을 편집할 수 있습니다 합니다 **가속기** 편집기입니다.

표준 속성 페이지를 사용 하려면 아래 절차 참조, 바로 편집 기능 및 방법 모두 결과가 동일 합니다. 변경 내용을 속성 페이지를 사용 하 여 또는 내부 편집을 사용 하 여 액셀러레이터 키 테이블에 즉시 반영 됩니다.

### <a name="to-edit-in-an-accelerator-table"></a>액셀러레이터 키 테이블에서 편집하려면

1. 액셀러레이터 키 테이블에서 해당 아이콘을 두 번 클릭 하 여 [리소스 뷰](../windows/resource-view-window.md)합니다.

1. 테이블에서 항목을 선택 하 고 내부 편집을 활성화 하려면 선택 합니다.

1. 드롭다운 콤보 상자에서 선택하거나 현재 위치에서 입력하여 변경합니다.

   - 에 대 한 **ID**목록 또는 편집 하는 형식 중에서 선택 합니다.

   - 에 대 한 **한정자**목록 중에서 선택 합니다.

   - 에 대 한 **키**목록 또는 편집 하는 형식 중에서 선택 합니다.

   - 에 대 한 **형식**를 선택 **ASCII** 하거나 **VIRTKEY** 목록에서.

### <a name="to-find-an-entry-in-an-open-accelerator-table"></a>열린 액셀러레이터 키 테이블에서 항목을 찾으려면

1. 액셀러레이터 키 테이블에서 해당 아이콘을 두 번 클릭 하 여 [리소스 뷰](../windows/resource-view-window.md)합니다.

1. 열 내용을 사전순으로 정렬 하려면 열 머리글을 선택 합니다. 예를 들어 선택할 **ID** 액셀러레이터 키 테이블의 모든 Id를 사전순으로 표시 합니다.

그런 다음 목록을 검색하고 항목을 찾을 수 있습니다.

### <a name="to-add-an-entry-to-an-accelerator-table"></a>액셀러레이터 키 테이블에 항목을 추가하려면

1. 액셀러레이터 키 테이블에서 해당 아이콘을 두 번 클릭 하 여 [리소스 뷰](../windows/resource-view-window.md)합니다.

1. 액셀러레이터 키 테이블 내에서 마우스 오른쪽 단추로 클릭 하 고 선택 **새 액셀러레이터 키** 바로 가기 메뉴에서 테이블의 맨 아래에 빈 행 항목을 선택 합니다.

1. 선택는 **ID** ID 드롭다운 목록에서 상자 또는에 새 ID를 입력 합니다 **ID** 상자.

1. 형식 합니다 **키** 액셀러레이터 키 또는 마우스 오른쪽 단추 클릭으로 사용 하 고 선택 하려는 **다음 입력 된 키** 키 조합을 설정 하려면 바로 가기 메뉴에서 (합니다 **다음 입력 된 키** 명령입니다 에서도 사용 가능 합니다 **편집** 메뉴).

1. 변경 된 **한정자** 하 고 **형식**필요한 경우.

1. **Enter** 키를 누릅니다.

   > [!NOTE]
   > 정의한 모든 액셀러레이터 키가 고유한지 확인합니다. 예를 들어 잘못 된 없습니다 효과가 적용 된 동일한 ID를 할당 하는 여러 키 조합이 할 수 있습니다 **Ctrl** + **P** 하 고 **F8** 둘 다 ID_PRINT에 할당 될 수 있습니다. 그러나 둘 이상의 ID 제대로 작동 하지 것입니다, 예를 들어 할당할 키 조합을 것 **Ctrl** + **Z** 가 ID_SPELL_CHECK와 ID_THESAURUS 모두에 할당 합니다.

### <a name="to-delete-an-entry-from-an-accelerator-table"></a>액셀러레이터 키 테이블에서 항목을 삭제하려면

1. 액셀러레이터 키 테이블에서 해당 아이콘을 두 번 클릭 하 여 [리소스 뷰](../windows/resource-view-window.md)합니다.

1. 삭제하려는 항목을 선택합니다. (누른 합니다 **Ctrl** 또는 **Shift** 여러 항목을 선택 하도록 선택 하는 동안 키입니다.)

1. 마우스 오른쪽 단추로 **삭제** 바로 가기 메뉴에서 (누르거나 **삭제** 에서 합니다 **편집** 메뉴).

> [!TIP]
> 삭제에 대 한 바로 가기 키를 누릅니다 하는 것은 **삭제** 키입니다.

### <a name="to-move-or-copy-an-accelerator-table-entry-to-another-resource-script-file"></a>액셀러레이터 키 테이블 항목을 다른 리소스 스크립트 파일로 이동/복사

1. 두 리소스 스크립트 파일 모두에서 액셀러레이터 키 테이블을 엽니다.

1. 이동하려는 항목을 선택합니다.

1. **편집할** 메뉴에서 선택 **복사** 또는 **잘라내기**합니다.

1. 대상 리소스 스크립트 파일에서 항목을 선택합니다.

1. **편집할** 메뉴 선택 **붙여넣기**합니다.

   > [!NOTE]
   > 복사 및 붙여넣기의 바로 가기 키를 사용할 수도 있습니다.

### <a name="to-change-the-properties-of-multiple-accelerator-keys"></a>여러 액셀러레이터 키 속성을 변경 하려면

1. 액셀러레이터 키 테이블에서 해당 아이콘을 두 번 클릭 하 여 [리소스 뷰](../windows/resource-view-window.md)합니다.

1. 액셀러레이터 키를 누른 채로 변경 하려면 선택 합니다 **Ctrl** 키를 선택 합니다.

1. 로 이동 합니다 [속성 창](/visualstudio/ide/reference/properties-window) 선택한 가속기 공유의 모든 값을 입력 합니다.

   > [!NOTE]
   > 각 한정자 값이 부울 속성으로 표시 합니다 **속성** 창입니다. 변경 하는 경우는 [한정자](../windows/accelerator-modifier-property.md) 값을 **속성** 창 액셀러레이터 키 테이블에서 새 한정자 있었습니까 이전에 한정자에는 추가으로 처리 합니다. 이 인해 모든 한정자 값을 설정 하는 경우 해야 모든 액셀러레이터 키를 동일한 공유 하는지 확인 하려면 모든 설정 **한정자** 설정 합니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고 항목

[리소스 편집기](../windows/resource-editors.md)<br/>
[미리 정의된 액셀러레이터 키](../windows/predefined-accelerator-keys.md)<br/>