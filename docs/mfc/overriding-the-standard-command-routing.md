---
title: 표준 명령 라우팅 재정의 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- MFC, command routing
- command routing [MFC], overriding
- command handling [MFC], routing commands
- overriding, standard command routing
ms.assetid: 872b698a-7432-40c4-9008-68721e8effa5
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 33ee603f680919d69684ab94acfa0515d3ec6292
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46439499"
---
# <a name="overriding-the-standard-command-routing"></a>표준 명령 라우팅 재정의

드문 경우에서 라우팅 표준 프레임 워크의 일부 변형을 구현 해야 하는 경우 재정의할 수 있습니다. 재정의 하 여 하나 이상의 클래스의 라우팅을 변경 하는 개념은 `OnCmdMsg` 해당 클래스에 있습니다. 이 수행 합니다.

- 기본이 아닌 개체에 전달 하는 순서를 무시 하는 클래스입니다.

- 새 기본이 아닌 개체에서 또는 명령 대상에서이 수에 명령을 전달할 합니다.

라우팅에 일부 새 개체를 삽입 하면 해당 클래스는 명령 대상 클래스 여야 합니다. 재정의 버전에서 `OnCmdMsg`를 재정의 하는 버전을 호출 해야 합니다. 참조를 [OnCmdMsg](../mfc/reference/ccmdtarget-class.md#oncmdmsg) 클래스의 멤버 함수 `CCmdTarget` 에 *MFC 참조* 와 같은 클래스의 버전 `CView` 및 `CDocument` 예제에 대 한 제공 된 소스 코드에서.

## <a name="see-also"></a>참고 항목

[프레임워크가 처리기를 호출하는 방법](../mfc/how-the-framework-calls-a-handler.md)

