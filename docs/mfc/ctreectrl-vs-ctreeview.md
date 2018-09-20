---
title: CTreeCtrl vs입니다. CTreeView | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
f1_keywords:
- CTreeCtrl
- CTreeView
dev_langs:
- C++
helpviewer_keywords:
- tree view controls
- CTreeCtrl class [MFC], vs. CTreeView class [MFC]
- CTreeView class [MFC], vs. CTreeCtrl class [MFC]
- tree controls [MFC], and tree view
ms.assetid: bba5af25-103f-4b53-84d3-071bc9bd6494
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: e8acaecbdfb99b8ae0b27023145a0ef6aee1f219
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46399153"
---
# <a name="ctreectrl-vs-ctreeview"></a>CTreeCtrl vs입니다. CTreeView

트리 컨트롤을 캡슐화 하는 두 개의 클래스를 제공 하는 MFC: [CTreeCtrl](../mfc/reference/ctreectrl-class.md) 하 고 [CTreeView](../mfc/reference/ctreeview-class.md)합니다. 각 클래스는 다양 한 상황에서 유용 합니다.

사용 하 여 `CTreeCtrl` 일반 자식 창 컨트롤에 필요한 경우 대화 상자에서 예를 들어 있습니다. 사용 하려는 특히 `CTreeCtrl` 일반적인 대화 상자와 같이 창에서 다른 자식 컨트롤이 될 경우.

사용 하 여 `CTreeView` 하려는 경우 문서/뷰 아키텍처의 보기 창 처럼 작동 하도록 트리 컨트롤 및 트리 컨트롤입니다. `CTreeView` 프레임 창 또는 분할자 창의 전체 클라이언트 영역을 차지 합니다. 부모 창의 크기를 조정 하 고 도구 모음, 메뉴 및 액셀러레이터 키에서 명령 메시지를 처리 하는 경우 자동으로 조정 됩니다. 해당 하는 문서 개체 트리를 표시 하는 데 필요한 데이터를 포함 하는 트리 컨트롤에 있으므로 복잡할 필요가 없습니다-도 사용할 수 있습니다 [CDocument](../mfc/reference/cdocument-class.md) 문서 템플릿의 문서 유형으로 합니다.

## <a name="see-also"></a>참고 항목

[CTreeCtrl 사용](../mfc/using-ctreectrl.md)<br/>
[컨트롤](../mfc/controls-mfc.md)

