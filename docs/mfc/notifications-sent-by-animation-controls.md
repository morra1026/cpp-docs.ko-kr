---
title: 애니메이션 컨트롤이 보내는 알림 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- notifications [MFC], animation controls
- CAnimateCtrl class [MFC], notifications
- controls [MFC], animation
- animation controls [MFC], notifications
ms.assetid: 584f5824-446b-4a1a-85f7-ef61842c8186
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: d7aff43577a4b1aa55fc0725ba4753228e334000
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43199663"
---
# <a name="notifications-sent-by-animation-controls"></a>애니메이션 컨트롤이 보내는 알림
애니메이션 컨트롤 ([CAnimateCtrl](../mfc/reference/canimatectrl-class.md)) 두 가지 유형의 알림 메시지를 보냅니다. 변경이 보내지기 형태로 [WM_COMMAND](/windows/desktop/menurc/wm-command) 메시지입니다.  
  
 합니다 [ACN_START](/windows/desktop/Controls/acn-start) 애니메이션 컨트롤 클립을 재생 시작 되었을 때 전송 됩니다. 합니다 [ACN_STOP](/windows/desktop/Controls/acn-stop) 애니메이션 컨트롤 완료 했거나 클립을 재생을 중지 하는 경우 전송 됩니다.  
  
## <a name="see-also"></a>참고 항목  
 [CAnimateCtrl 사용](../mfc/using-canimatectrl.md)   
 [컨트롤](../mfc/controls-mfc.md)

