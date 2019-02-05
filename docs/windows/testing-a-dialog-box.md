---
title: 대화 상자 (c + +) 디자인
ms.date: 11/04/2016
helpviewer_keywords:
- Test Dialog command
- testing, dialog boxes
- dialog boxes [C++], testing
- dialog boxes [C++], size
- dialog boxes [C++], positioning
ms.assetid: 45034ee9-c554-4f4b-8c46-6ddefdee8951
ms.openlocfilehash: 4a879f6bb1cdcd4b4897e510fb21d04500dfd3f2
ms.sourcegitcommit: 52c05e10b503e834c443ef11e7ca1987e332f876
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/05/2019
ms.locfileid: "55742689"
---
# <a name="designing-a-dialog-box-c"></a>대화 상자 (c + +) 디자인

위치 및 크기의 c + + 대화 상자, 위치 및 안에 있는 컨트롤의 크기는 대화 단위로 측정 됩니다. 개별 컨트롤 및 대화 상자에 대 한 값은 Visual Studio 상태를 선택 하면 표시줄의 오른쪽 아래에 나타납니다.

대화 상자를 디자인할 때 시뮬레이션 수 및 프로그램을 컴파일하지 않고 런타임에 동작을 테스트 해야 합니다. 이 모드에서 다음 작업을 수행할 수 있습니다.

- 텍스트 입력, 콤보 상자 목록에서 선택, 옵션 켜기 또는 끄기, 명령 선택

- 탭 순서 테스트

- 라디오 단추 또는 확인란과 같은 컨트롤의 그룹화 테스트

- 대화 상자의 컨트롤에 대한 바로가기 키 테스트

   > [!NOTE]
   > 마법사를 사용하여 만든 대화 상자 코드에 대한 연결은 시뮬레이션에 포함되지 않습니다.

대화 상자를 테스트할 때는 일반적으로 주 프로그램 창을 기준으로 상대적인 위치에 표시됩니다. 대화 상자를 설정한 경우 **Absolute Align** 속성을 **True**를 화면의 왼쪽 위 모퉁이 기준으로 하는 위치에 있는 대화 상자에 표시 됩니다.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index)합니다.

## <a name="to-specify-the-location-and-size-of-a-dialog-box"></a>대화 상자의 크기와 위치를 지정 하려면

세 가지 속성에 설정할 수 있는 합니다 [속성 창](/visualstudio/ide/reference/properties-window) 대화 상자가 화면 표시를 지정 합니다. 합니다 **Center** 속성은 부울; 값을 설정 하는 경우 **True**, 대화 상자 화면 중앙에 항상 표시 됩니다. 설정 하면 **False**를 설정할 수 있습니다 합니다 **XPos** 및 **YPos** 화면 대화 상자를 표시할 위치를 명시적으로 정의 하는 속성입니다. 위치 속성으로 정의 된 보기 영역의 왼쪽 위 모서리에서 오프셋된 값은 `{X=0, Y=0}`합니다. 위치를 기준으로 합니다 **Absolute Align** 속성: 경우 **True**, 좌표는 화면을 기준으로 하는 경우 **False**, 대화 상자를 기준으로 좌표는 소유자 창입니다.

## <a name="to-test-a-dialog-box"></a>대화 상자를 테스트하려면

1. 경우는 **대화 상자** 편집기가 활성 창, 메뉴 모음에서 선택 합니다 **형식** > **테스트 대화 상자**합니다.

1. 시뮬레이션을 종료 하려면 키를 누릅니다 **Esc**를 선택 하거나 합니다 **닫기** 테스트 하는 대화 상자에서 단추입니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고 항목

[대화 상자의 컨트롤](../windows/controls-in-dialog-boxes.md)<br/>
[대화 상자 편집기](../windows/dialog-editor.md)<br/>
[대화 상자 편집기 도구 모음 표시 또는 숨기기](../windows/showing-or-hiding-the-dialog-editor-toolbar.md)