---
title: 열 컨트롤에 추가 (보고서 뷰) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- CListCtrl class [MFC], adding columns
- report view in CListCtrl class [MFC]
- views [MFC], report
- columns [MFC], adding to CListCtrl
- CListCtrl class [MFC], report view
ms.assetid: 7392c0d7-f8a5-4e7b-9ae7-b53dc9dd80ae
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: c3e81de52856d67760ffe58f29e4c39ac79213c4
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43221946"
---
# <a name="adding-columns-to-the-control-report-view"></a>컨트롤에 열 추가(보고서 뷰)
> [!NOTE]
>  다음 절차 중 하나에 적용 됩니다는 [CListView](../mfc/reference/clistview-class.md) 하거나 [CListCtrl](../mfc/reference/clistctrl-class.md) 개체입니다.  
  
 목록 컨트롤을 보고서 보기의 경우 각 목록 컨트롤 항목의 다양 한 하위 항목을 구성 하는 메서드를 제공 합니다. 열 표시 됩니다. 이 조직 목록 컨트롤의 열과 연결 된 목록 컨트롤 항목의 하위 항목 사이 일대일 대응을 사용 하 여 구현 됩니다. 하위 항목에 대 한 자세한 내용은 참조 하세요. [컨트롤에 항목 추가](../mfc/adding-items-to-the-control.md)합니다. 보고서 뷰의 목록 컨트롤의 예로 Windows 95 및 Windows 98 탐색기 세부 정보 보기에서 제공 됩니다. 첫 번째 열에는 폴더, 파일 아이콘 및 레이블 나열합니다. 다른 열 파일 크기, 파일 형식, 마지막으로 수정한 날짜 및 등을 나열 합니다.  
  
 컨트롤에 있는 경우에 열은 표시 열 언제 든 지 목록 컨트롤을 추가할 수 있습니다, 있지만 `LVS_REPORT` 스타일 비트를 설정 합니다.  
  
 각 열에 연관 된 헤더 항목 (참조 [CHeaderCtrl](../mfc/reference/cheaderctrl-class.md)) 열을 레이블 및 사용자가 열 크기를 조정할 수 있도록 하는 개체입니다.  
  
 목록 컨트롤에서 보고서 보기를 지 원하는 경우에 목록 컨트롤 항목의 각 하위 항목에 대 한 열을 추가 해야 합니다. 준비 하 여 열을 추가 합니다.는 [LV_COLUMN](/windows/desktop/api/commctrl/ns-commctrl-taglvcolumna) 구조 및에 대 한 호출을 설정한 후 [열 삽입](../mfc/reference/clistctrl-class.md#insertcolumn)합니다. (헤더 항목 이라고 함) 하는 데 필요한 열을 추가한 후 다시 정렬할 수 있습니다 이러한 멤버 함수 및 포함 된 헤더 컨트롤에 속하는 스타일을 사용 하 여 합니다. 자세한 내용은 [헤더 컨트롤에서 항목 순서 지정](../mfc/ordering-items-in-the-header-control.md)합니다.  
  
> [!NOTE]
>  목록 컨트롤을 사용 하 여 만들어지는 경우 합니다 **LVS_NOCOLUMNHEADER** 스타일 열을 삽입 하려는 시도 무시 됩니다.  
  
## <a name="see-also"></a>참고 항목  
 [CListCtrl 사용](../mfc/using-clistctrl.md)   
 [컨트롤](../mfc/controls-mfc.md)

