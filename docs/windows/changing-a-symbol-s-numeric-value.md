---
title: 기호 변경&#39;숫자 값 s | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: conceptual
f1_keywords:
- vc.editors.symbol.changing.value
dev_langs:
- C++
helpviewer_keywords:
- numeric values
- symbols, numeric values
- numeric values, changing symbols
ms.assetid: 468e903b-9c07-4251-ae09-3b6cb754cc2b
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: c05c732f87434754fb6776d7f914b4ffa5c26015
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43219278"
---
# <a name="changing-a-symbol39s-numeric-value"></a>기호 변경&#39;가 숫자 값

단일 리소스와 연결 된 기호를 사용할 수 있습니다 합니다 [속성 창](/visualstudio/ide/reference/properties-window) 기호 값을 변경 합니다. 사용할 수는 [리소스 기호 대화 상자](../windows/resource-symbols-dialog-box.md) 리소스에 할당 되어 있지 않은 기호의 값을 변경 합니다. 자세한 내용은 [할당 되지 않은 기호 변경](../windows/changing-unassigned-symbols.md)합니다.

### <a name="to-change-a-symbol-value-assigned-to-a-single-resource-or-object"></a>단일 리소스 또는 개체에 할당된 기호 값을 변경하려면

1. [리소스 뷰](../windows/resource-view-window.md), 리소스를 선택 합니다.

   > [!NOTE]
   > 프로젝트에 .rc 파일이 아직 없는 경우 [새 리소스 스크립트 파일 만들기](../windows/how-to-create-a-resource-script-file.md)를 참조하세요.

2. 에 **속성** 창, 형식 기호 이름 뒤에 등호 기호와 정수를 합니다 **ID** 상자 예를 들어:

    ```
    IDC_EDITNAME=5100
    ```

새 값은 다음에 프로젝트를 저장할 때 기호 헤더 파일에 저장됩니다. 기호 이름만 ID 상자에 표시되고, 유효성 검사가 완료된 후에는 등호 기호와 값이 표시되지 않습니다.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 리소스에 액세스 하는 관리 되는 프로젝트에 리소스 파일을 수동으로 추가 하는 방법은 속성에 문자열, 정적 리소스 표시 및 리소스를 할당 합니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고 항목

[기호 값 제한](../windows/symbol-value-restrictions.md)  
[미리 정의된 기호 ID](../windows/predefined-symbol-ids.md)