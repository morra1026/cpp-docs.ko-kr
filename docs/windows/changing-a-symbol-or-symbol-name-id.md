---
title: 기호 변경
ms.date: 11/04/2016
f1_keywords:
- vc.editors.symbol.changing
- vc.editors.symbol.restrictions.name
- vc.editors.symbol.changing.value
- vc.editors.symbol.restrictions.value
- vc.editors.symbol.changing.header
helpviewer_keywords:
- symbol names
- symbols [C++], names
- restrictions, symbol names
- numeric values
- symbols [C++], numeric values
- numeric values, changing symbols
- symbols [C++], value restrictions
- restrictions, symbol values
- resource files [C++], multiple
- Resource Includes dialog box [C++]
- symbol header files [C++], changing names
- symbols [C++], symbol header files
- Resource.h
ms.assetid: 26541832-8dba-4177-b642-e08f94502ea7
ms.openlocfilehash: 7d2890c2d2c05f1ee0309446dfe2de9917f85707
ms.sourcegitcommit: 63c072f5e941989636f5a2b13800b68bb7129931
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/06/2019
ms.locfileid: "55763988"
---
# <a name="changing-a-symbol"></a>기호 변경

새 리소스 또는 리소스 개체를 만들 때 개발 환경에서 IDD_DIALOG1과 같은 기본 기호 이름을 할당합니다. 사용할 수는 [속성 창](/visualstudio/ide/reference/properties-window) 기본 기호 이름을 변경 하거나 이미 리소스와 연결 된 기호의 이름을 변경 합니다.

단일 리소스와 연결 된 기호를 사용할 수도 있습니다는 **속성** 기호 값을 변경 하는 창입니다. 사용할 수는 [리소스 기호 대화 상자](../windows/resource-symbols-dialog-box.md) 리소스에 할당 되어 있지 않은 기호의 값을 변경 합니다. 자세한 내용은 [할당 되지 않은 기호 변경](../windows/changing-unassigned-symbols.md)합니다.

일반적으로 모든 기호 정의에 저장 됩니다 `Resource.h`합니다. 그러나 예를 들어 같은 디렉터리에서 둘 이상의 리소스 파일을 사용할 수 있도록 이 포함 파일 이름을 변경해야 할 수 있습니다.

관리되는 프로젝트에 리소스를 추가하는 방법에 대한 내용은 *.NET 프레임워크 개발자 가이드*의 [데스크톱 앱의 리소스](/dotnet/framework/resources/index)를 참조하세요.

## <a name="to-change-a-resources-symbol-name-id"></a>리소스 기호 이름 (ID)를 변경 하려면

1. [리소스 뷰](../windows/resource-view-window.md), 리소스를 선택 합니다.

   > [!NOTE]
   > 프로젝트에 .rc 파일이 아직 없는 경우 [새 리소스 스크립트 파일 만들기](../windows/how-to-create-a-resource-script-file.md)를 참조하세요.

1. 에 **속성** 창에서 새 기호 이름을 입력 하거나 기존 기호 목록에서 선택 합니다 **ID** 상자입니다.

   새 기호 이름을 입력하는 경우 값이 자동으로 할당됩니다.

사용할 수는 [리소스 기호 대화 상자](../windows/resource-symbols-dialog-box.md) 리소스에 할당 되지 않은 기호의 이름을 변경할 수 있습니다. 자세한 내용은 [할당 되지 않은 기호 변경](../windows/changing-unassigned-symbols.md)합니다.

### <a name="symbol-name-restrictions"></a>기호 이름 제한

기호 이름에 대한 제한은 다음과 같습니다.

- 모든 [기호](../windows/symbols-resource-identifiers.md) 응용 프로그램의 범위 내에서 고유 해야 합니다. 이렇게 하면 헤더 파일에서 기호 정의 충돌을 방지할 수 있습니다.

- 기호 이름에 유효한 문자는 A-Z, a-z, 0-9 및 밑줄(_)입니다.

- 기호 이름은 숫자로 시작할 수 없으며 247자로 제한됩니다.

- 기호 이름에는 공백을 사용할 수 없습니다.

- 기호 이름은 대/소문자를 구분하지 않지만 첫 번째 기호 정의의 대/소문자는 유지됩니다. 기호를 정의하는 헤더 파일은 리소스 컴파일러/편집기 및 C++ 프로그램에서 리소스 파일에 정의된 리소스를 참조하는 데 사용됩니다. 대/소문자만 다른 두 기호 이름에 대해 C++ 프로그램은 별도의 두 기호로 보지만 리소스 컴파일러/편집기는 두 이름이 하나의 단일 기호를 나타내는 것으로 봅니다.

   > [!NOTE]
   > 아래에 간략하게 설명된 표준 기호 이름 체계(ID*_[keyword])를 따르지 않고 기호 이름이 리소스 스크립트 컴파일러에 알려진 키워드와 동일한 경우 리소스 스크립트 파일을 빌드하려고 하면 진단하기 어려운 임의 오류가 생성될 수 있습니다. 이를 방지하려면 표준 이름 지정 체계를 준수하세요.

기호 이름에는 해당 이름이 나타내는 리소스 또는 개체의 종류를 나타내는 설명 접두사가 있습니다. 이러한 설명 접두사는 텍스트 조합 ID로 시작합니다. MFC(Microsoft Foundation Class) 라이브러리는 다음 표에 표시된 기호 명명 규칙을 사용합니다.

|범주|접두사|사용|
|--------------|------------|---------|
|자료|IDR_ IDD_ IDC_ IDI_ IDB_|액셀러레이터 키 또는 메뉴(및 연결된 리소스 또는 사용자 지정 리소스) 대화 상자 커서 아이콘 비트맵|
|메뉴 항목|ID_|Menu item|
|명령|ID_|명령|
|컨트롤 및 자식 창|IDC_|Control|
|문자열|IDS_|문자열 테이블의 문자열|
|MFC|AFX_|미리 정의된 MFC 기호에 예약됨|

## <a name="to-change-a-symbol-value-assigned-to-a-single-resource-or-object"></a>단일 리소스 또는 개체에 할당된 기호 값을 변경하려면

1. [리소스 뷰](../windows/resource-view-window.md), 리소스를 선택 합니다.

   > [!NOTE]
   > 프로젝트에 .rc 파일이 아직 없는 경우 [새 리소스 스크립트 파일 만들기](../windows/how-to-create-a-resource-script-file.md)를 참조하세요.

1. 에 **속성** 창, 형식 기호 이름 뒤에 등호 기호와 정수를 합니다 **ID** 상자 예를 들어:

    ```
    IDC_EDITNAME=5100
    ```

새 값은 다음에 프로젝트를 저장할 때 기호 헤더 파일에 저장됩니다. 기호 이름만 ID 상자에 표시되고, 유효성 검사가 완료된 후에는 등호 기호와 값이 표시되지 않습니다.

### <a name="symbol-value-restrictions"></a>기호 값 제한

기호 값은 #define 전처리기 지시문에 대해 일반적인 방식으로 표현된 정수일 수 있습니다. 다음은 기호 값의 몇 가지 예입니다.

```
18
4001
0x0012
-3456
```

리소스(액셀러레이터 키, 비트맵, 커서, 대화 상자, 아이콘, 메뉴, 문자열 테이블 및 버전 정보)에 대한 기호 값은 0에서 32,767 사이의 10진수여야 하며 16진수일 수 없습니다. 대화 상자 컨트롤이나 문자열 테이블의 개별 문자열 같이 리소스 일부에 대한 기호 값은 0에서 65,534 사이이거나 -32,768에서 32,767 사이일 수 있습니다.

리소스 기호는 16비트 숫자입니다. 이 기호는 부호 있는 숫자나 부호 없는 숫자로 입력할 수 있지만 내부적으로는 부호 없는 정수로 사용됩니다. 따라서 음수는 해당 양수 값으로 캐스팅됩니다.

다음은 기호 값에 대한 몇 가지 제한 사항입니다.

- Visual Studio 개발 환경 및 MFC에서는 일부 숫자 범위를 특별한 용도로 사용합니다. 가장 중요한 비트 세트를 사용하는 모든 숫자(부호에 따라 -32,768 ~ -1 또는 32,768 ~ 65,534)는 MFC에 의해 예약되었습니다.

- 기호 값은 다른 기호 문자열을 사용하여 정의할 수 없습니다. 예를 들어 다음과 같은 기호 정의는 지원되지 않습니다.

    ```cpp
    #define IDC_MYEDIT  IDC_OTHEREDIT  //not supported
    ```

- 인수가 있는 전처리기 매크로는 값 정의로 사용할 수 없습니다. 예를 들어:

    ```cpp
    #define   IDD_ABOUT  ID(7) //not supported
    ```

   컴파일 시간에 `ID`가 계산되는 결과에 관계없이 유효한 식이 아닙니다.

- 응용 프로그램에 식으로 정의된 기호를 포함하는 기존 파일이 있을 수 있습니다. 읽기 전용 기호로 포함 하는 방법에 대 한 자세한 내용은 참조 하세요. [공유 (읽기 전용) 또는 계산 된 기호](../windows/including-shared-read-only-or-calculated-symbols.md)합니다.

숫자 범위에 대 한 자세한 내용은 참조 하세요. [TN023: 표준 MFC 리소스](../mfc/tn023-standard-mfc-resources.md)합니다.

## <a name="to-change-the-name-of-the-resource-symbol-header-file"></a>리소스 기호 헤더 파일의 이름을 변경하려면

1. [리소스 뷰](../windows/resource-view-window.md).rc 파일을 마우스 오른쪽 단추로 클릭 하 고 선택 [리소스 내용](../windows/resource-includes-dialog-box.md) 바로 가기 메뉴에서.

   > [!NOTE]
   > 프로젝트에 .rc 파일이 아직 없는 경우 [새 리소스 스크립트 파일 만들기](../windows/how-to-create-a-resource-script-file.md)를 참조하세요.

1. 에 **기호 헤더 파일** 포함 파일에 대 한 새 이름을 입력 합니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고자료

[미리 정의된 기호 ID](../windows/predefined-symbol-ids.md)<br/>
[리소스 기호 보기](../windows/viewing-resource-symbols.md)<br/>
