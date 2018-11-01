---
title: ATL 메시지 처리기 추가
ms.date: 11/04/2016
helpviewer_keywords:
- message handlers [C++]
- ATL, windows
- message handling [C++], ATL message handler
- windows [C++], ATL
- ATL, message handlers
ms.assetid: cdea38a1-0d9b-4f8d-bbd5-b4f063fb3eeb
ms.openlocfilehash: 6d812c70e7cec4739ee9477d30ad9744b4fddc50
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50565501"
---
# <a name="adding-an-atl-message-handler"></a>ATL 메시지 처리기 추가

컨트롤에 메시지 처리기 (Windows 메시지를 처리 하는 멤버 함수)를 추가 하려면 먼저 클래스 뷰에서 컨트롤을 선택 합니다. 엽니다는 **속성** 창에서를 **메시지** 아이콘과 반대 되는 필수 메시지 상자에서 드롭다운 컨트롤 클릭 합니다. 컨트롤의 헤더 파일과 컨트롤.cpp 파일에서 처리기의 기본 구현에서 메시지 처리기에 대 한 선언을 추가 합니다. 또한 메시지 맵에 추가 하 고 처리기에 대 한 항목을 추가 합니다.

ATL에서 메시지 처리기를 추가 하는 것을 MFC 클래스에 메시지 처리기를 추가 하는 것과 비슷합니다. 참조 [MFC 메시지 처리기 추가](../mfc/reference/adding-an-mfc-message-handler.md) 자세한 내용은 합니다.

ATL 메시지 처리기 추가에 다음 조건이 적용 됩니다.

- 메시지 처리기 MFC로 동일한 명명 규칙을 따릅니다.

- 새 메시지 맵 항목은 기본 메시지 맵에 추가 됩니다. 대체 메시지 맵 및 연결에 마법사를 인식 하지 못합니다.

## <a name="see-also"></a>참고 항목

[창 구현](../atl/implementing-a-window.md)

