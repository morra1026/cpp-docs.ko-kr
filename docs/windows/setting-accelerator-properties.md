---
title: 액셀러레이터 키 속성 (c + +)를 설정합니다.
ms.date: 11/04/2016
helpviewer_keywords:
- accelerator properties
- properties [C++], accelerator properties
- Type property
- Key property
- Modifier property
- VIRTKEY
- Key property
- ID property
ms.assetid: 0fce9156-3025-4e18-b034-e219a4c65812
ms.openlocfilehash: e1fac31635b7ccc09f9c184cf734fa4f7717cb97
ms.sourcegitcommit: 5beace7dcc6bf0e8b8cc96a930e7424f9daa05cb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2019
ms.locfileid: "55232138"
---
# <a name="setting-accelerator-properties"></a>액셀러레이터 키 속성 설정

액셀러레이터 키 속성을 설정할 수 있습니다 합니다 [속성 창](/visualstudio/ide/reference/properties-window) 언제 든 지 합니다. 사용할 수도 있습니다는 [액셀러레이터 키 편집기](../windows/accelerator-editor.md) 액셀러레이터 키 테이블에서 액셀러레이터 키 속성을 수정 합니다. 사용 하 여 변경 합니다 **속성** 창 또는 **가속기** 편집기는 동일한 결과 얻은: 편집 액셀러레이터 키 테이블에 바로 반영 됩니다.

## <a name="id-property"></a>ID 속성

합니다 **ID** 프로그램 코드에서 각 액셀러레이터 키 테이블 항목을 참조 하는 속성입니다. 이 항목에는 프로그램의 액셀러레이터 키 또는 키 조합을 누를 때 받을 명령 값입니다. 메뉴 항목 동일 액셀러레이터 키를 확인, 하 게 해당 Id 동일 (액셀러레이터 키 테이블의 ID 메뉴 리소스에 대 한 ID와 동일).

속성은 세 가지 각 액셀러레이터 ID에 대 한:는 **한정자** 속성을 **키** 속성 및 **형식** 속성입니다.

## <a name="modifier-property"></a>Modifier 속성

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

## <a name="key-property"></a>키 속성

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

## <a name="type-property"></a>Type 속성

합니다 **형식** 속성은 액셀러레이터 키 ID와 연결 된 바로 가기 키 조합을 ASCII/ANSI 키 값을 또는 가상 키 (VIRTKEY) 조합으로 해석할지 결정 합니다.

- 경우는 **형식** 속성이 ASCII를 **한정자** 속성 수만 있습니다 `None` 또는 `Alt`를 사용 하는 액셀러레이터 키를 가질 수 있는 **Ctrl** (키 지정 된 키 앞에 `^`).

- 경우는 **형식** 속성은 VIRTKEY를 조합 `Modifier` 및 `Key` 값이 잘못 되었습니다.

> [!NOTE]
> 액셀러레이터 키 테이블에 값을 입력 하 고 값이 ASCII/ANSI 간단히 클릭으로 처리 하려는 경우는 **형식** 드롭다운 목록에서에서 선택 ASCII 테이블의 항목에 대 한 합니다. 그러나 사용 하는 경우는 **다음 입력 된 키** 명령 (**편집** 메뉴) 지정 하는 `Key`를 변경 해야 합니다는 **형식** ascii VIRTKEY속성*하기 전에* 입력을 `Key` 코드입니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고자료

[액셀러레이터 키 테이블에서 편집](../windows/editing-in-an-accelerator-table.md)<br/>
[미리 정의된 액셀러레이터 키](../windows/predefined-accelerator-keys.md)<br/>
[리소스 편집기](../windows/resource-editors.md)<br/>
