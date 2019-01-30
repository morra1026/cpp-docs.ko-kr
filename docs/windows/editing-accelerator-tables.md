---
title: 액셀러레이터 키 테이블 편집 (c + +)
ms.date: 11/04/2016
f1_keywords:
- vc.editors.accelerator
helpviewer_keywords:
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
ms.assetid: 56e24efb-d06b-4ed9-8915-1f99f725e247
ms.openlocfilehash: dfa0c26132378bcbe8a7f5203351134d91746aa7
ms.sourcegitcommit: 5beace7dcc6bf0e8b8cc96a930e7424f9daa05cb
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2019
ms.locfileid: "55232177"
---
# <a name="editing-accelerator-tables-c"></a>액셀러레이터 키 테이블 편집 (c + +)

C + + 프로젝트에서 직접 사용 하 여 현재 위치에서 편집 액셀러레이터 키 테이블을 편집할 수 있습니다 합니다 **가속기** 편집기입니다.

표준 속성 페이지를 사용 하려면 아래 절차 참조, 바로 편집 기능 및 방법 모두 결과가 동일 합니다. 변경 내용을 속성 페이지를 사용 하 여 또는 내부 편집을 사용 하 여 액셀러레이터 키 테이블에 즉시 반영 됩니다.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대한 내용은 [데스크톱 앱에 대한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)를 참조하세요. 관리되는 앱의 전역화 및 지역화 리소스에 대한 내용은 [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index)을 참조하세요.

> [!NOTE]
> 프로젝트에 .rc 파일이 아직 없는 경우 [새 리소스 스크립트 파일 만들기](../windows/how-to-create-a-resource-script-file.md)를 참조하세요.

## <a name="to-edit-in-an-accelerator-table"></a>액셀러레이터 키 테이블에서 편집하려면

1. 액셀러레이터 키 테이블에서 해당 아이콘을 두 번 클릭 하 여 [리소스 뷰](../windows/resource-view-window.md)합니다.

1. 테이블에서 항목을 선택 하 고 내부 편집을 활성화 하려면 선택 합니다.

1. 드롭다운 콤보 상자에서 선택하거나 현재 위치에서 입력하여 변경합니다.

   - 에 대 한 [ID](id-property.md)목록 또는 편집 하는 형식 중에서 선택 합니다.

   - 에 대 한 [한정자](../windows/accelerator-modifier-property.md)목록 중에서 선택 합니다.

   - 에 대 한 [키](../windows/accelerator-key-property.md)목록 또는 편집 하는 형식 중에서 선택 합니다.

   - 에 대 한 [형식](../windows/accelerator-type-property.md)를 선택 **ASCII** 하거나 **VIRTKEY** 목록에서.

## <a name="to-find-an-entry-in-an-open-accelerator-table"></a>열린 액셀러레이터 키 테이블에서 항목을 찾으려면

1. 액셀러레이터 키 테이블에서 해당 아이콘을 두 번 클릭 하 여 [리소스 뷰](../windows/resource-view-window.md)합니다.

1. 열 내용을 사전순으로 정렬 하려면 열 머리글을 선택 합니다. 예를 들어 선택할 **ID** 액셀러레이터 키 테이블의 모든 Id를 사전순으로 표시 합니다.

그런 다음 목록을 검색하고 항목을 찾을 수 있습니다.

## <a name="to-add-an-entry-to-an-accelerator-table"></a>액셀러레이터 키 테이블에 항목을 추가하려면

1. 액셀러레이터 키 테이블에서 해당 아이콘을 두 번 클릭 하 여 [리소스 뷰](../windows/resource-view-window.md)합니다.

1. 액셀러레이터 키 테이블 내에서 마우스 오른쪽 단추로 클릭 하 고 선택 **새 액셀러레이터 키** 바로 가기 메뉴에서 테이블의 맨 아래에 빈 행 항목을 선택 합니다.

1. 선택는 [ID](id-property.md) ID 드롭다운 목록에서 상자 또는에 새 ID를 입력 합니다 **ID** 상자.

1. 형식 합니다 [키](../windows/accelerator-key-property.md) 액셀러레이터 키 또는 마우스 오른쪽 단추 클릭으로 사용 하 고 선택 하려는 **다음 입력 된 키** 키 조합을 설정 하려면 바로 가기 메뉴에서 (합니다 **다음 입력 된 키** 명령입니다 에서도 사용 가능 합니다 **편집** 메뉴).

1. 변경 된 [한정자](../windows/accelerator-modifier-property.md) 하 고 [형식](../windows/accelerator-type-property.md)필요한 경우.

1. **Enter** 키를 누릅니다.

   > [!NOTE]
   > 정의한 모든 액셀러레이터 키가 고유한지 확인합니다. 예를 들어 잘못 된 없습니다 효과가 적용 된 동일한 ID를 할당 하는 여러 키 조합이 할 수 있습니다 **Ctrl** + **P** 하 고 **F8** 둘 다 ID_PRINT에 할당 될 수 있습니다. 그러나 둘 이상의 ID 제대로 작동 하지 것입니다, 예를 들어 할당할 키 조합을 것 **Ctrl** + **Z** 가 ID_SPELL_CHECK와 ID_THESAURUS 모두에 할당 합니다.

## <a name="to-delete-an-entry-from-an-accelerator-table"></a>액셀러레이터 키 테이블에서 항목을 삭제하려면

1. 액셀러레이터 키 테이블에서 해당 아이콘을 두 번 클릭 하 여 [리소스 뷰](../windows/resource-view-window.md)합니다.

1. 삭제하려는 항목을 선택합니다. (누른 합니다 **Ctrl** 또는 **Shift** 여러 항목을 선택 하도록 선택 하는 동안 키입니다.)

1. 마우스 오른쪽 단추로 **삭제** 바로 가기 메뉴에서 (누르거나 **삭제** 에서 합니다 **편집** 메뉴).

\- 또는 -

- 키를 눌러 합니다 **삭제** 키입니다.

## <a name="to-move-or-copy-an-accelerator-table-entry-to-another-resource-script-file"></a>액셀러레이터 키 테이블 항목을 다른 리소스 스크립트 파일로 이동/복사

1. 두 리소스 스크립트 파일 모두에서 액셀러레이터 키 테이블을 엽니다.

1. 이동하려는 항목을 선택합니다.

1. **편집할** 메뉴에서 선택 **복사** 또는 **잘라내기**합니다.

1. 대상 리소스 스크립트 파일에서 항목을 선택합니다.

1. **편집할** 메뉴 선택 **붙여넣기**합니다.

   > [!NOTE]
   > 복사 및 붙여넣기의 바로 가기 키를 사용할 수도 있습니다.

## <a name="to-change-the-properties-of-multiple-accelerator-keys"></a>여러 액셀러레이터 키 속성을 변경 하려면

1. 액셀러레이터 키 테이블에서 해당 아이콘을 두 번 클릭 하 여 [리소스 뷰](../windows/resource-view-window.md)합니다.

1. 액셀러레이터 키를 누른 채로 변경 하려면 선택 합니다 **Ctrl** 키를 선택 합니다.

1. 로 이동 합니다 [속성 창](/visualstudio/ide/reference/properties-window) 선택한 가속기 공유의 모든 값을 입력 합니다.

   > [!NOTE]
   > 각 한정자 값이 부울 속성으로 표시 합니다 **속성** 창입니다. 변경 하는 경우는 [한정자](../windows/accelerator-modifier-property.md) 값을 **속성** 창 액셀러레이터 키 테이블에서 새 한정자 있었습니까 이전에 한정자에는 추가으로 처리 합니다. 이 인해 모든 한정자 값을 설정 하는 경우 해야 모든 액셀러레이터 키를 동일한 공유 하는지 확인 하려면 모든 설정 **한정자** 설정 합니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고 항목

[액셀러레이터 키 편집기](../windows/accelerator-editor.md)<br/>
[리소스 편집기](../windows/resource-editors.md)
