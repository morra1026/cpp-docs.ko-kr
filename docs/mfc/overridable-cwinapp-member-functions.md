---
title: 재정의 가능 CWinApp 멤버 함수
ms.date: 11/04/2016
f1_keywords:
- CWinApp
helpviewer_keywords:
- overriding [MFC], overridable functions in CWinApp
- application class [MFC]
- CWinApp class [MFC], overridables
ms.assetid: 07183d5e-734b-45d9-a8b6-9dde4adac0b4
ms.openlocfilehash: 9f1098e305606df9463e308466b7864b019d5a00
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50459282"
---
# <a name="overridable-cwinapp-member-functions"></a>재정의 가능 CWinApp 멤버 함수

[CWinApp](../mfc/reference/cwinapp-class.md) 몇 가지 키 재정의 가능한 멤버 함수를 제공 (`CWinApp` 클래스에서 이러한 멤버를 재정의 [CWinThread](../mfc/reference/cwinthread-class.md), 올 `CWinApp` 파생):

- [InitInstance](../mfc/initinstance-member-function.md)

- [실행](../mfc/run-member-function.md)

- [ExitInstance](../mfc/exitinstance-member-function.md)

- [OnIdle](../mfc/onidle-member-function.md)

재정의해야 하는 유일한 `CWinApp` 멤버 함수는 `InitInstance`입니다.

## <a name="see-also"></a>참고 항목

[CWinApp: 응용 프로그램 클래스](../mfc/cwinapp-the-application-class.md)
