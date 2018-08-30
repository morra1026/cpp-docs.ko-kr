---
title: 헤더 컨트롤에 항목 추가 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- controls [MFC], header
- CHeaderCtrl class [MFC], adding items
- header controls [MFC], adding items to
ms.assetid: 2e9a28b1-7302-4a93-8037-c5a4183e589a
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: a6450d99b8df436c64337e52fc14244ecbb0edfc
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43206149"
---
# <a name="adding-items-to-the-header-control"></a>헤더 컨트롤에 항목 추가
헤더 컨트롤을 만든 후 ([CHeaderCtrl](../mfc/reference/cheaderctrl-class.md)) 해당 부모 창에서 항목을 추가할 "헤더" 필요에 따라: 열당 하나에 일반적으로 합니다.  
  
### <a name="to-add-a-header-item"></a>헤더 항목을 추가 하려면  
  
1.  준비 된 [HD_ITEM](/windows/desktop/api/commctrl/ns-commctrl-_hd_itema) 구조입니다.  
  
2.  호출 [CHeaderCtrl::InsertItem](../mfc/reference/cheaderctrl-class.md#insertitem), 구조를 전달 합니다.  
  
3.  추가 항목에 대 한 1 및 2 단계를 반복 합니다.  
  
 자세한 내용은 [헤더 컨트롤에 항목 추가](/windows/desktop/Controls/header-controls) Windows sdk에서입니다.  
  
## <a name="see-also"></a>참고 항목  
 [CHeaderCtrl 사용](../mfc/using-cheaderctrl.md)   
 [컨트롤](../mfc/controls-mfc.md)

