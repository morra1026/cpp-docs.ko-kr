---
title: 대화 상자 제거
ms.date: 11/04/2016
helpviewer_keywords:
- dialog boxes [MFC], deleting
- destruction, dialog box
- dialog boxes [MFC], destroying
- dialog boxes [MFC], removing
- modeless dialog boxes [MFC], destroying
- MFC dialog boxes [MFC], destroying
- modal dialog boxes [MFC], destroying
ms.assetid: dabceee7-3639-4d85-bf34-73515441b3d0
ms.openlocfilehash: f84e36a2a002610c294653012c40707fddcaba54
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50607469"
---
# <a name="destroying-the-dialog-box"></a>대화 상자 제거

일반적으로 모달 대화 상자 스택 프레임에 생성 되어를 만든 함수가 종료 될 때 소멸 합니다. 대화 상자 개체의 소멸자는 개체 범위를 벗어날 때 호출 됩니다.

모덜리스 대화 상자는 일반적으로 만들고 부모 뷰나 프레임 창을 소유-응용 프로그램의 주 프레임 창 또는 문서 프레임 창입니다. 기본값 [OnClose](../mfc/reference/cwnd-class.md#onclose) 처리기 호출 [DestroyWindow](../mfc/reference/cwnd-class.md#destroywindow), 대화 상자 창에는 제거 합니다. 대화 상자를 독립적으로 또는 기타 특수 소유권 의미 체계에 없는 대 한 포인터를 사용 하 여 실행을 하는 경우를 재정의 해야 [PostNcDestroy](../mfc/reference/cwnd-class.md#postncdestroy) 를 c + + 대화 상자 개체를 제거 합니다. 또한 재정의 해야 [OnCancel](../mfc/reference/cdialog-class.md#oncancel) 호출 `DestroyWindow` 에서 그 합니다. 그렇지 않은 경우 더 이상 필요한 경우 대화 상자의 소유자 c + + 개체를 제거 해야 합니다.

## <a name="see-also"></a>참고 항목

[대화 상자의 수명 주기](../mfc/life-cycle-of-a-dialog-box.md)

