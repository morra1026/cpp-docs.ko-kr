---
title: 프레임 창 클래스 (아키텍처) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
f1_keywords:
- vc.classes.frame
dev_langs:
- C++
helpviewer_keywords:
- frame window classes [MFC], document/view architecture
ms.assetid: 5da01fb4-f531-46cc-914f-e422e4f07f5d
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 117554b2c34853aa166c12d80b4821d3721e5992
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46394129"
---
# <a name="frame-window-classes-architecture"></a>프레임 창 클래스(아키텍처)

문서/뷰 아키텍처, 프레임 창에는 뷰 창을 포함 하는 windows. 또한 지원 제어 하지 막대에 연결 합니다.

여러 문서 MDI (인터페이스) 응용 프로그램에서 주 창에서 파생 된 `CMDIFrameWnd`합니다. 이 간접적으로 포함 되는 문서 프레임 `CMDIChildWnd` 개체입니다. `CMDIChildWnd` 개체의 문서 뷰를 포함 합니다.

단일 문서 인터페이스 (SDI) 응용 프로그램 주 창에서 파생 된 `CFrameWnd`, 현재 문서의 뷰를 포함 합니다.

[CFrameWnd](../mfc/reference/cframewnd-class.md)<br/>
SDI 응용 프로그램의 주 프레임 창에 대 한 기본 클래스입니다. 기본 다른 모든 프레임 창 클래스에 대 한 클래스는 또한만 합니다.

[CMDIFrameWnd](../mfc/reference/cmdiframewnd-class.md)<br/>
MDI 응용 프로그램의 주 프레임 창에 대 한 기본 클래스입니다.

[CMDIChildWnd](../mfc/reference/cmdichildwnd-class.md)<br/>
MDI 응용 프로그램의 문서 프레임 창에 대 한 기본 클래스입니다.

[COleIPFrameWnd](../mfc/reference/coleipframewnd-class.md)<br/>
준비에서 서버 문서를 편집 하는 경우 프레임 창 보기를 제공 합니다.

## <a name="see-also"></a>참고 항목

[클래스 개요](../mfc/class-library-overview.md)

