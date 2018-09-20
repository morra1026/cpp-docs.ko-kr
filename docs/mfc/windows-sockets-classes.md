---
title: Windows 소켓 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
f1_keywords:
- vc.classes.net
dev_langs:
- C++
helpviewer_keywords:
- sockets classes [MFC]
- Windows Sockets [MFC], classes
ms.assetid: 58b9ab8d-9e44-4db3-8265-e04e713d2e9a
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 893fa525b04376cde0e96f280c95e6bfd1243946
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46439980"
---
# <a name="windows-sockets-classes"></a>Windows 소켓 클래스

Windows 소켓 두 컴퓨터 간에 통신 하는 네트워크 프로토콜 독립적인 방식으로 제공 합니다. 이러한 소켓 동기적 일 수 있습니다 (프로그램 통신이 완료 될 때까지 대기) 또는 비동기 (프로그램 계속 통신 진행 되는 동안 실행).

[CAsyncSocket](../mfc/reference/casyncsocket-class.md)<br/>
Windows 소켓 API에서 씬 래퍼를 캡슐화합니다.

[CSocket](../mfc/reference/csocket-class.md)<br/>
파생 된 상위 수준 추상화 `CAsyncSocket`합니다. 동기적으로 작동합니다.

[CSocketFile](../mfc/reference/csocketfile-class.md)<br/>
제공 된 `CFile` Windows 소켓 인터페이스입니다.

## <a name="see-also"></a>참고 항목

[클래스 개요](../mfc/class-library-overview.md)

