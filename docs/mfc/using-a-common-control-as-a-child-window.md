---
title: 공용 컨트롤을 사용 하 여 자식 창으로 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- controls [MFC], using as child windows
- windows [MFC], common controls as
- child windows [MFC], common controls as
- common controls [MFC], child windows
- Windows common controls [MFC], child windows
ms.assetid: 608f7d47-7854-4fce-bde9-856c51e76753
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 73ddb010aeb8190c063d2691806e3ebd89d0f744
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46417971"
---
# <a name="using-a-common-control-as-a-child-window"></a>공용 컨트롤을 자식 창으로 사용

Windows 공용 컨트롤 중 하나는 다른 모든 창의 자식 창으로 사용할 수 있습니다. 다음 절차에는 동적으로 공용 컨트롤을 만들고 다음 사용 하는 방법을 설명 합니다.

### <a name="to-use-a-common-control-as-a-child-window"></a>공용 컨트롤을 자식 창으로 사용 하려면

1. 관련된 클래스 또는 처리기에서 컨트롤을 정의 합니다.

1. 컨트롤의 재정의 사용 합니다 [CWnd::Create](../mfc/reference/cwnd-class.md#create) Windows 컨트롤을 만드는 방법.

1. 컨트롤이 만들어진 후 (만큼는 `OnCreate` 처리기 경우 하위 컨트롤), 해당 멤버 함수를 사용 하 여 컨트롤을 조작할 수 있습니다. 개별 컨트롤에 대 한 설명은 참조 하세요 [컨트롤](../mfc/controls-mfc.md) 메서드에 대 한 자세한 내용은 합니다.

1. 사용 하 여 컨트롤을 사용 하 여 마쳤으면 [CWnd::DestroyWindow](../mfc/reference/cwnd-class.md#destroywindow) 컨트롤을 삭제 하려면.

## <a name="see-also"></a>참고 항목

[컨트롤 만들기 및 사용](../mfc/making-and-using-controls.md)<br/>
[컨트롤](../mfc/controls-mfc.md)

