---
title: 트리 컨트롤 항목 선택 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- tree controls [MFC], item selection
- controls [MFC], selecting items in
- CTreeCtrl class [MFC], item selection
- item selection in tree controls
ms.assetid: 7bcb3b16-b9c8-4c06-9350-7bc3c1c5009b
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: fd6632a44dd4806b8f13683b50cad76b5eebe27a
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43212583"
---
# <a name="tree-control-item-selection"></a>트리 컨트롤 항목 선택
선택 영역이 한 항목에서 다른 트리 컨트롤을 변경 하는 경우 ([CTreeCtrl](../mfc/reference/ctreectrl-class.md)) 보냅니다 [TVN_SELCHANGING](/windows/desktop/Controls/tvn-selchanging) 하 고 [TVN_SELCHANGED](/windows/desktop/Controls/tvn-selchanged) 알림 메시지입니다. 두 알림에 변경 마우스 클릭 이나 키 입력과의 결과 인지 여부를 지정 하는 값을 포함 합니다. 알림을 선택이 취소 하는 항목 및 선택 손실 되는 항목에 대 한 정보도 포함 합니다. 항목의 선택 상태에 종속 된 항목 특성을 설정 하려면이 정보를 사용할 수 있습니다. 반환 **TRUE** 대 한 응답으로 `TVN_SELCHANGING` 방지 선택 항목 변경; 반환 **FALSE** 변경 수 있습니다.  
  
 응용 프로그램 호출 하 여 선택을 변경할 수는 [SelectItem](../mfc/reference/ctreectrl-class.md#selectitem) 멤버 함수입니다.  
  
## <a name="see-also"></a>참고 항목  
 [CTreeCtrl 사용](../mfc/using-ctreectrl.md)   
 [컨트롤](../mfc/controls-mfc.md)

