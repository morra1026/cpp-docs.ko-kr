---
title: 컨트롤 선택
ms.date: 11/04/2016
helpviewer_keywords:
- Dialog Editor [C++], selecting controls
- dominant controls
- dialog box controls [C++], selecting in editor
- controls [C++], selecting
- size, controls
- controls [C++], dominant
- controls [C++], removing from groups
- Dialog Editor [C++], dominant control
ms.assetid: 27f05450-4550-4229-9f4c-2c9e06365596
ms.author: Michael.Blome
ms.topic: tutorial
ms.service: cpp
author: mikeblome
ms.openlocfilehash: 008c99ae4b2cba5ff8f8b9ab069bb1b8085b7524
ms.sourcegitcommit: b488462a6e035131121e6f32d8f3b108cc798b5e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55293639"
---
# <a name="selecting-controls"></a>컨트롤 선택

컨트롤 크기를 선택, 정렬, 이동, 복사 또는 삭제할 수 및 다음 작업을 완료 합니다. 대부분의 경우에서에서 크기 조정 및 맞춤 도구를 사용 하려면 둘 이상의 컨트롤을 선택 해야 합니다 [대화 상자 편집기 도구 모음](../windows/showing-or-hiding-the-dialog-editor-toolbar.md)합니다.

컨트롤이 선택 되는 음영 처리 된 주위에 테두리가 실선 (활성) 또는 비어 있는 (비활성)는 제곱 작은 "크기 조정 핸들을" 하는 경우 선택 테두리에 표시 합니다. 여러 컨트롤을 선택 하면 기준 컨트롤에 단색 크기 조정 핸들 있고 다른 선택된 된 컨트롤이 모두 속이 빈 크기 조정 핸들입니다.

크기를 조정 하거나 여러 개의 컨트롤을 정렬 하는 경우는 **대화** 편집기 "기준 컨트롤"을 사용 하 여 다른 컨트롤의 크기와 정렬 하는 방법을 확인 하려면. 기본적으로 주요 컨트롤에는 선택한 첫 번째 컨트롤이입니다.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework Developer's Guide*합니다. 수동으로 관리되는 프로젝트에 리소스 파일을 추가, 리소스 액세스, 정적 리소스 표시 및 속성에 리소스 문자열 할당에 대한 내용은 [데스크톱 앱에 대한 리소스 파일 만들기](/dotnet/framework/resources/creating-resource-files-for-desktop-apps)를 참조하세요. 관리되는 앱의 전역화 및 지역화 리소스에 대한 내용은 [Globalizing and Localizing .NET Framework Applications](/dotnet/standard/globalization-localization/index)을 참조하세요.

## <a name="to-select-multiple-controls"></a>여러 컨트롤을 선택 하려면

1. 에 [도구 상자 창](/visualstudio/ide/reference/toolbox)를 선택 합니다 **포인터** 도구입니다.

1. 대화 상자에서 선택 하려는 컨트롤 주위의 선택 상자에 대 한 포인터를 끕니다.

   마우스 단추를 놓으면 모든 내부 및 선택 상자는 선택한 교차 제어 합니다.

   \- 또는 -

   누른 합니다 **Shift** 키 및 선택 영역에 포함 하려는 컨트롤을 선택 합니다.

   \- 또는 -

   누른 합니다 **Ctrl** 키 및 선택 영역에 포함 하려는 컨트롤을 선택 합니다.

## <a name="to-remove-a-control-from-a-group-of-selected-controls-or-to-add-a-control-to-a-group-of-selected-controls"></a>선택한 컨트롤의 그룹에서 컨트롤을 제거 하려면 또는 그룹 선택된 된 컨트롤에 컨트롤을 추가 하려면

1. 선택한 컨트롤의 그룹을 사용 하 여 길게 누른 합니다 **Shift** 키를 기존 선택 항목에 추가 하거나 제거할 하려는 컨트롤을 선택 합니다.

   > [!NOTE]
   > 누른 합니다 **Ctrl** 키 및 선택 영역 내에 있는 컨트롤을 선택 하면 선택에서 기준 컨트롤을 제어 하는 확인 됩니다.

## <a name="to-specify-the-dominant-control"></a>기준 컨트롤 지정

1. 누른 합니다 **Ctrl** 크기와 다른 컨트롤의 위치를 정하는 데 사용 하려는 컨트롤을 클릭 하 고 키 *첫 번째*입니다.

> [!NOTE]
> 기준 컨트롤의 크기 조정 핸들은 하위 컨트롤의 핸들은 속이 빈 실선입니다. 모든 크기 조정 이나 맞춤 기준 컨트롤을 기반으로 합니다.

## <a name="to-change-the-dominant-control"></a>기준 컨트롤을 변경 하려면

1. 현재 선택된 된 컨트롤이 모두 외부를 클릭 하 여 현재 선택을 모두 취소 합니다.

1. 다른 컨트롤을 먼저 선택 하면 이전 절차를 반복 합니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고 항목

[대화 상자의 컨트롤](../windows/controls-in-dialog-boxes.md)<br/>
[컨트롤](../mfc/controls-mfc.md)