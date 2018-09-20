---
title: 코드 마법사 하지 않고 컨트롤에 대 한 형식이 안전한 액세스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- dialog boxes [MFC], accessing controls
- dialog box controls [MFC], accessing
ms.assetid: 325b4927-d49b-42b4-8e0b-fc84f31fb059
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 2685c946b9ee1c738ee83f9413b7fd955857febb
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46438342"
---
# <a name="type-safe-access-to-controls-without-code-wizards"></a>코드 마법사를 사용하지 않고 컨트롤에 대한 형식이 안전한 액세스 수행

컨트롤에 대 한 형식이 안전한 액세스를 만드는 첫 번째 방법은 인라인 멤버 함수를 사용 하 여 클래스의 반환 형식으로 캐스팅할 `CWnd`의 `GetDlgItem` 이 예제와 같이 적절 한 c + + 컨트롤 형식, 멤버 함수:

[!code-cpp[NVC_MFCControlLadenDialog#50](../mfc/codesnippet/cpp/type-safe-access-to-controls-without-code-wizards_1.cpp)]

그런 다음 다음과 유사한 코드를 사용 하 여 형식이 안전한 방식으로 액세스를 제어 하려면이 멤버 함수를 사용할 수 있습니다.

[!code-cpp[NVC_MFCControlLadenDialog#51](../mfc/codesnippet/cpp/type-safe-access-to-controls-without-code-wizards_2.cpp)]

## <a name="see-also"></a>참고 항목

[대화 상자의 컨트롤에 대한 형식이 안전한 액세스](../mfc/type-safe-access-to-controls-in-a-dialog-box.md)<br/>
[코드 마법사를 사용하여 컨트롤에 대한 형식이 안전한 액세스 수행](../mfc/type-safe-access-to-controls-with-code-wizards.md)

