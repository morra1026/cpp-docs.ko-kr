---
title: 바로 가기 키 설정
ms.date: 11/04/2016
helpviewer_keywords:
- keyboard shortcuts [MFC], hot keys
- access keys [MFC], hot keys
- CHotKeyCtrl class [MFC], setting hot key
ms.assetid: 6f3bc141-e346-4dce-9ca7-3e6b2c453f3f
ms.openlocfilehash: ebaddb4a64a4d9d47b82fd36f118c74527554e53
ms.sourcegitcommit: c85c8a1226d8fbbaa29f4691ed719f8e6cc6575c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54893226"
---
# <a name="setting-a-hot-key"></a>바로 가기 키 설정

응용 프로그램 바로 가기 키를 제공 하는 정보를 사용할 수 있습니다 ([CHotKeyCtrl](../mfc/reference/chotkeyctrl-class.md))의 두 가지 방법으로 제어 합니다.

- 전송 하 여 비 자식 창을 활성화 하기 위한 전역 바로 가기 키를 설정 된 [WM_SETHOTKEY](/windows/desktop/inputdev/wm-sethotkey) 활성화할 창에 메시지.

- Windows 함수를 호출 하 여 스레드 관련 바로 가기 키를 설정 [RegisterHotKey](/windows/desktop/api/winuser/nf-winuser-registerhotkey)합니다.

## <a name="see-also"></a>참고 항목

[CHotKeyCtrl 사용](../mfc/using-chotkeyctrl.md)<br/>
[컨트롤](../mfc/controls-mfc.md)

