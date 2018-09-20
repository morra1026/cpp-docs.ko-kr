---
title: 재정의 가능 CWinApp 멤버 함수 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
f1_keywords:
- CWinApp
dev_langs:
- C++
helpviewer_keywords:
- overriding [MFC], overridable functions in CWinApp
- application class [MFC]
- CWinApp class [MFC], overridables
ms.assetid: 07183d5e-734b-45d9-a8b6-9dde4adac0b4
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: ced9d7d5f7f49df50e028a299f83ddebdc9fc2d1
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46395136"
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
