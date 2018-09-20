---
title: 헤더 컨트롤에서 항목 순서 지정 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
f1_keywords:
- DS_DRAGDROP
dev_langs:
- C++
helpviewer_keywords:
- sequence [MFC]
- sequence [MFC], header control items
- OrderToIndex method [MFC]
- DS_DRAGDROP notification [MFC]
- GetOrderArray method [MFC]
- SetOrderArray method [MFC]
- header controls [MFC], ordering items
ms.assetid: 5aaef872-75b5-49c5-8fed-6f9a81fca812
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: f446eb557fab4f4ff6396042e832e4584546bd96
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46416827"
---
# <a name="ordering-items-in-the-header-control"></a>헤더 컨트롤에서 항목 순서 지정

했으면 [헤더 컨트롤에 항목 추가](../mfc/adding-items-to-the-header-control.md)를 조작 하거나 다음 함수를 사용 하 여 순서에 대 한 정보를 얻을 수 있습니다.

- [CHeaderCtrl::GetOrderArray](../mfc/reference/cheaderctrl-class.md#getorderarray) 고 [CHeaderCtrl::SetOrderArray](../mfc/reference/cheaderctrl-class.md#setorderarray)

     검색 하 고 헤더 항목의 왼쪽에서 오른쪽 순서를 설정 합니다.

- [CHeaderCtrl::OrderToIndex](../mfc/reference/cheaderctrl-class.md#ordertoindex)합니다.

     특정 헤더 항목에 대 한 인덱스 값을 검색합니다.

멤버 함수는 이전 하는 것 외에도 HDS_DRAGDROP 스타일에는 헤더 컨트롤 내의 머리글 항목을 끌어다 사용자 수 있습니다. 자세한 내용은 [헤더 항목에 대 한 끌어서 놓기 지원 제공](../mfc/providing-drag-and-drop-support-for-header-items.md)합니다.

## <a name="see-also"></a>참고 항목

[CHeaderCtrl 사용](../mfc/using-cheaderctrl.md)

