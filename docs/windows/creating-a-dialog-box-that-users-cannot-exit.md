---
title: 종료할 수 없는 사용자가 대화 상자 (c + +) 만들기
ms.date: 11/04/2016
helpviewer_keywords:
- dialog boxes [C++], creating
- modal dialog boxes [C++], logon screens
- logon screens
ms.assetid: 54823c27-1658-4388-bd12-0a1ce8f3899e
ms.openlocfilehash: 83c6c099f3d39db66969371e2cf7ad99a7f08587
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50579844"
---
# <a name="creating-a-dialog-box-c-that-users-cannot-exit"></a>종료할 수 없는 사용자가 대화 상자 (c + +) 만들기

사용자가 종료할 수 없는 런타임 대화 상자를 만들 수 있습니다. 이 종류의 대화 상자는 로그온에 유용하며, 응용 프로그램 또는 문서를 잠그는 데에도 유용합니다.

### <a name="to-create-a-dialog-box-that-a-user-cannot-exit"></a>사용자가 종료할 수 없는 대화 상자를 만들려면

1. 대화 상자의 **속성** 창에서 **시스템 메뉴** 속성을 **false**로 설정합니다.

   이렇게 하면 대화 상자의 시스템 메뉴 및 **닫기** 단추가 비활성화됩니다.

2. 대화 상자 폼에서 **취소** 및 **확인** 단추를 삭제합니다.

   런타임 시 사용자는 이러한 특징이 있는 모달 대화 상자를 종료할 수 없습니다.

테스트 대화 상자는 검색 될 때 대화 상자의 이러한 종류의 테스트를 사용 하려면 **Esc** 눌러져 있습니다. (**Esc** VK_ESCAPE 가상 키라고도 하는 것이 라고도 합니다.) 런타임에 동작 대화 상자는 디자인 하는 방법에 관계 없이 종료할 수 있습니다 테스트 모드에서 키를 눌러 **Esc**합니다.

> [!NOTE]
> MFC 응용 프로그램에 대 한 사용자가 종료할 수 없습니다. 대화 상자를 만들려면 재정의 해야의 기본 동작 `OnOK` 하 고 `OnCancel` 키를 눌러 대화 상자를 닫을 여전히 수 연결된 단추를 삭제 하는 경우에 하기 때문에  **입력** 나 **Esc**합니다.

관리 되는 프로젝트에 리소스를 추가 하는 방법에 대 한 정보를 참조 하세요 [데스크톱 앱의 리소스](/dotnet/framework/resources/index)합니다.

## <a name="requirements"></a>요구 사항

Win32

## <a name="see-also"></a>참고 항목

[방법: 리소스 파일 만들기](../windows/how-to-create-a-resource.md)<br/>
[리소스 파일](../windows/resource-files-visual-studio.md)<br/>
[대화 상자 편집기](../windows/dialog-editor.md)