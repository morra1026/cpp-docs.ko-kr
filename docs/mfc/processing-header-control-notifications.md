---
title: 헤더 컨트롤 알림 처리
ms.date: 11/04/2016
helpviewer_keywords:
- CHeaderCtrl class [MFC], processing notifications
- controls [MFC], header
- notifications [MFC], processing for CHeaderCtrl
- header controls [MFC], processing notifications
- header control notifications
ms.assetid: e6c6af7c-d458-4d33-85aa-48014ccde5f6
ms.openlocfilehash: 4513bafedd531c7f0bcb103728c19c0940a2efc9
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50626774"
---
# <a name="processing-header-control-notifications"></a>헤더 컨트롤 알림 처리

뷰 또는 대화 상자 클래스에서 속성 창을 만드는 데는 [OnChildNotify](../mfc/reference/cwnd-class.md#onchildnotify) 처리기 함수를 모든 헤더 컨트롤에 대 한 switch 문 ([CHeaderCtrl](../mfc/reference/cheaderctrl-class.md)) 하려는 알림 메시지 처리 (참조 [함수에 메시지 매핑](../mfc/reference/mapping-messages-to-functions.md)). 사용자가 클릭 하거나 항목 간 구분선을 끌기 머리글 항목을 두 번 클릭할 때 부모 창에 알림이 전송 됩니다.

헤더 컨트롤에 연결 된 알림 메시지에 나열 됩니다 [헤더 컨트롤 참조](https://msdn.microsoft.com/library/windows/desktop/bb775239) Windows SDK에 있습니다.

## <a name="see-also"></a>참고 항목

[CHeaderCtrl 사용](../mfc/using-cheaderctrl.md)<br/>
[컨트롤](../mfc/controls-mfc.md)

