---
title: 창 개체 제거
ms.date: 11/04/2016
helpviewer_keywords:
- frame windows [MFC], destroying
- window objects [MFC], deleting
- window objects [MFC], destroying
- window objects [MFC], removing
ms.assetid: 3241fea0-c614-4a25-957d-20f21bd5fd0c
ms.openlocfilehash: 363ff2a4cee48b1660de87714d73c93e795017cd
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50488811"
---
# <a name="destroying-window-objects"></a>창 개체 제거

주의 해야 자신의 자식 창을 사용 하 여 사용자가 창을 사용 하 여 완료 하는 경우 c + + 창 개체를 삭제 하려면. 이러한 개체를 소멸 되지 않습니다 하는 경우 응용 프로그램의 메모리를 복구 되지 않습니다. 다행 스럽게도 프레임 워크는 프레임 창, 뷰 및 대화 상자에 대 한 작성 뿐만 아니라 창 소멸을 관리합니다. 추가 windows를 만든 있다면 제거 하는 일을 담당 합니다.

## <a name="what-do-you-want-to-know-more-about"></a>자세히 알아보려는 항목

- [창 소멸 시퀀스](../mfc/window-destruction-sequence.md)

- [할당 및 창 메모리 할당 취소](../mfc/allocating-and-deallocating-window-memory.md)

- [해당 HWND에서에서 CWnd 분리](../mfc/detaching-a-cwnd-from-its-hwnd.md)

- [일반 창 만들기 시퀀스](../mfc/general-window-creation-sequence.md)

- [프레임 창 제거](../mfc/destroying-frame-windows.md)

## <a name="see-also"></a>참고 항목

[창 개체](../mfc/window-objects.md)

