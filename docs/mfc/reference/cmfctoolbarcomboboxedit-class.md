---
title: CMFCToolBarComboBoxEdit 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: reference
f1_keywords:
- CMFCToolBarComboBoxEdit
- AFXTOOLBARCOMBOBOXBUTTON/CMFCToolBarComboBoxEdit
- AFXTOOLBARCOMBOBOXBUTTON/CMFCToolBarComboBoxEdit::CMFCToolBarComboBoxEdit
dev_langs:
- C++
helpviewer_keywords:
- CMFCToolBarComboBoxEdit [MFC], CMFCToolBarComboBoxEdit
ms.assetid: 4789c34a-ce58-48ba-a26f-38748b601352
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 554fcb68583b6d7b00e57a5df814fe0330069426
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45721970"
---
# <a name="cmfctoolbarcomboboxedit-class"></a>CMFCToolBarComboBoxEdit 클래스
프레임 워크를 사용 하는 `CMFCToolBarComboBoxEdit` 는 편집할 수 있는 콤보 상자 컨트롤 처럼 동작 하는 도구 모음 단추를 만드는 클래스입니다.  
  
## <a name="syntax"></a>구문  
  
```  
class CMFCToolBarComboBoxEdit : public CEdit  
```  
  
## <a name="members"></a>멤버  
  
### <a name="public-constructors"></a>Public 생성자  
  
|이름|설명|  
|----------|-----------------|  
|[CMFCToolBarComboBoxEdit::CMFCToolBarComboBoxEdit](#cmfctoolbarcomboboxedit)|`CMFCToolBarComboBoxEdit` 개체를 생성합니다.|  
|`CMFCToolBarComboBoxEdit::~CMFCToolBarComboBoxEdit`|소멸자|  
  
### <a name="public-methods"></a>Public 메서드  
  
|이름|설명|  
|----------|-----------------|  
|`CMFCToolBarComboBoxEdit::PreTranslateMessage`|디스패치 되기 전에 창 메시지를 변환 합니다 [TranslateMessage](/windows/desktop/api/winuser/nf-winuser-translatemessage) 하 고 [DispatchMessage](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) Windows 함수입니다. ( [CWnd::PreTranslateMessage](../../mfc/reference/cwnd-class.md#pretranslatemessage)를 재정의합니다.)|  
  
### <a name="remarks"></a>설명  
 클래스를 파생 합니다 `CMFCToolBarComboBoxEdit` 해당 편집 작업을 사용자 지정 클래스입니다.  
  
## <a name="inheritance-hierarchy"></a>상속 계층  
 [CObject](../../mfc/reference/cobject-class.md)  
  
 [CCmdTarget](../../mfc/reference/ccmdtarget-class.md)  
  
 [CWnd](../../mfc/reference/cwnd-class.md)  
  
 [CEdit](../../mfc/reference/cedit-class.md)  
  
 [CMFCToolBarComboBoxEdit](../../mfc/reference/cmfctoolbarcomboboxedit-class.md)  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** afxtoolbarcomboboxbutton.h  
  
##  <a name="cmfctoolbarcomboboxedit"></a>  CMFCToolBarComboBoxEdit::CMFCToolBarComboBoxEdit  
 `CMFCToolBarComboBoxEdit` 개체를 생성합니다.  
  
```  
CMFCToolBarComboBoxEdit(CMFCToolBarComboBoxButton& combo);
```  
  
### <a name="parameters"></a>매개 변수  
*콤보*<br/>
[in] 에 대 한 참조를 [CMFCToolBarComboBoxButton](../../mfc/reference/cmfctoolbarcomboboxbutton-class.md) 개체 콤보 상자 컨트롤을 포함 하는 도구 모음 단추입니다.  
  
### <a name="example"></a>예제  
 다음 예제에서는의 개체를 생성 하는 방법에 설명 합니다 `CMFCToolBarComboBoxEdit` 클래스입니다. 이 코드 조각은의 일부인 합니다 [IE 데모 샘플](../../visual-cpp-samples.md)합니다.  
  
 [!code-cpp[NVC_MFC_IEDemo#5](../../mfc/reference/codesnippet/cpp/cmfctoolbarcomboboxedit-class_1.cpp)]  
  
## <a name="see-also"></a>참고 항목  
 [계층 구조 차트](../../mfc/hierarchy-chart.md)   
 [클래스](../../mfc/reference/mfc-classes.md)   
 [CMFCToolBarComboBoxButton 클래스](../../mfc/reference/cmfctoolbarcomboboxbutton-class.md)
