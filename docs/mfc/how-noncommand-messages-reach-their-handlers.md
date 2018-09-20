---
title: 명령이 아닌 메시지가 해당 처리기에 도달 하는 방법 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- messages [MFC], routing
- noncommand messages
- Windows messages [MFC], routing
- message handling [MFC], noncommand messages
ms.assetid: e7df8aef-9fae-41f4-9c11-881d8465f602
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: b5c38a1d4294993170cfeff64be6a83700fa7497
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46373440"
---
# <a name="how-noncommand-messages-reach-their-handlers"></a>명령이 아닌 메시지가 해당 처리기에 도달하는 방법

명령과 달리 표준 Windows 메시지의 명령 체인 대상을 통해 라우트되지 않습니다 하지만 Windows에서 메시지를 보낼 창에서 일반적으로 처리 됩니다. 창을 주 프레임 창, MDI 자식 창, 표준 컨트롤, 대화 상자, 뷰 또는 일부 다른 자식 창의 종류가 수 있습니다.

런타임 시 각 Windows에 연결 되는 창 개체 (에서 직접 또는 간접적으로 파생 `CWnd`) 자체 연결 된 메시지 맵 및 처리기 함수가 포함 합니다. 프레임 워크가 메시지 맵을 사용해-명령을와-들어오는 메시지 처리기를 매핑할 합니다.

## <a name="see-also"></a>참고 항목

[프레임워크가 처리기를 호출하는 방법](../mfc/how-the-framework-calls-a-handler.md)

