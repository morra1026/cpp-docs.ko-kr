---
title: CWnd를 해당 HWND에서 분리
ms.date: 11/04/2016
f1_keywords:
- CWnd
helpviewer_keywords:
- HWND, detaching CWnd from
- removing HWNDs from CWnds
- CWnd objects [MFC], detaching from HWND
- detaching CWnds from HWNDs
- Detach method (CWnd class)
ms.assetid: 6efadf84-0517-4a3f-acfd-216e088f19c6
ms.openlocfilehash: fe4d9efa6adcec51d5944755e4a8abb1cc0784e4
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50653975"
---
# <a name="detaching-a-cwnd-from-its-hwnd"></a>CWnd를 해당 HWND에서 분리

개체-우회 해야 할 경우`HWND` 관계, MFC를 통해 다른 `CWnd` 멤버 함수 [분리](../mfc/reference/cwnd-class.md#detach)는 c + + 창 개체 Windows 창에서 연결을 끊습니다. 이 개체가 소멸 될 때 Windows 창을 제거에서 소멸자를 방지 합니다.

## <a name="what-do-you-want-to-know-more-about"></a>자세히 알아보려는 항목

- [창 만들기](../mfc/creating-windows.md)

- [창 소멸 시퀀스](../mfc/window-destruction-sequence.md)

- [할당 및 창 메모리 할당 취소](../mfc/allocating-and-deallocating-window-memory.md)

## <a name="see-also"></a>참고 항목

[창 개체](../mfc/window-objects.md)

