---
title: 목록 컨트롤 제거 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- list controls [MFC], destroying
- CListCtrl class [MFC], destroying controls
ms.assetid: 513ec820-3a02-49d2-b073-a6a7a3fc91b3
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 25642357e3dd9117ae2817307ed5fa3c4a0921d0
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46424543"
---
# <a name="destroying-the-list-control"></a>목록 컨트롤 제거

포함 하는 경우에 [CListCtrl](../mfc/reference/clistctrl-class.md) 개체 뷰 또는 대화 상자 클래스의 데이터 멤버와 해당 소유자가 제거 될 때 제거 됩니다. 사용 하는 경우는 [CListView](../mfc/reference/clistview-class.md), 프레임 워크 뷰를 제거 하는 경우 컨트롤을 제거 합니다.

목록 컨트롤 보다는 응용 프로그램에서 저장할 목록 데이터 중 일부에 대해 정렬 하는 경우 해당 할당 취소에 대 한 정렬 해야 합니다. 자세한 내용은 [콜백 항목 및 콜백 마스크](/windows/desktop/Controls/using-list-view-controls) Windows SDK에 있습니다.

또한 모든 이미지 목록 컨트롤을 만들어 list 컨트롤 개체를 사용 하 여 연결을 할당 취소에 대 한 담당 합니다.

## <a name="see-also"></a>참고 항목

[CListCtrl 사용](../mfc/using-clistctrl.md)<br/>
[컨트롤](../mfc/controls-mfc.md)

