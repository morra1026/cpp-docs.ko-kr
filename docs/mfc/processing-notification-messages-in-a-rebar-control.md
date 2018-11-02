---
title: Rebar 컨트롤에서 알림 메시지 처리
ms.date: 11/04/2016
helpviewer_keywords:
- RBN_ notification messages, description of
- CReBarCtrl class [MFC], notification messages sent by
- RBN_ notification messages [MFC]
- notifications [MFC], CReBarCtrl
ms.assetid: 40f43a60-0c18-4d8d-8fab-213a095624f9
ms.openlocfilehash: 8cbe9849e16e8bfa9c0d0ce1f96e846bffaab2ef
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50621834"
---
# <a name="processing-notification-messages-in-a-rebar-control"></a>Rebar 컨트롤에서 알림 메시지 처리

Rebar 컨트롤의 부모 클래스를 만듭니다는 `OnChildNotify` 모든 rebar 컨트롤에 대 한 switch 문 사용 하 여 처리기 함수 (`CReBarCtrl`) 알림 메시지를 처리 합니다. 사용자가 변경 내용 삭제 rebar 밴드의 레이아웃 및 등 rebar 컨트롤에서 밴드 rebar 컨트롤 위로 개체를 끌 때 부모 창에 알림이 전송 됩니다.

Rebar 컨트롤 개체에 의해 다음 알림 메시지를 보낼 수 있습니다.

- RBN_AUTOSIZE rebar 컨트롤 (RBS_AUTOSIZE 스타일으로 생성 됨)를 보낸 경우 rebar 자동 크기를 조정 합니다.

- RBN_BEGINDRAG 밴드를 끌기 시작할 때 rebar 컨트롤에서 전송 합니다.

- RBN_CHILDSIZE 밴드의 자식 창 크기를 조정할 때 rebar 컨트롤에서 전송 합니다.

- RBN_DELETEDBAND rebar 컨트롤 밴드를 삭제 한 다음 보냅니다.

- RBN_DELETINGBAND 밴드 삭제 되려고 할 때 rebar 컨트롤에서 전송 합니다.

- RBN_ENDDRAG 사용자가 밴드를 끌기를 중지 하면 rebar 컨트롤에서 보냅니다.

- RBN_GETOBJECT (RBS_REGISTERDROP 스타일을 사용 하 여 만든) rebar 컨트롤에서 전송 되는 개체를 컨트롤에서 밴드 위로 끌 때.

- RBN_HEIGHTCHANGE rebar 컨트롤 높이가 변경 될 때 보냅니다.

- RBN_LAYOUTCHANGED 사용자 컨트롤의 밴드 레이아웃을 변경할 때 rebar 컨트롤에서 보냅니다.

이러한 알림에 대 한 자세한 내용은 참조 하세요. [Rebar 컨트롤 참조](https://msdn.microsoft.com/library/windows/desktop/bb774375) Windows SDK에 있습니다.

## <a name="see-also"></a>참고 항목

[CReBarCtrl 사용](../mfc/using-crebarctrl.md)<br/>
[컨트롤](../mfc/controls-mfc.md)

