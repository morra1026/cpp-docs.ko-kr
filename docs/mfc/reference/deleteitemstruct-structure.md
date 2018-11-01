---
title: DELETEITEMSTRUCT 구조체
ms.date: 11/04/2016
f1_keywords:
- DELETEITEMSTRUCT
helpviewer_keywords:
- DELETEITEMSTRUCT structure [MFC]
ms.assetid: 48d3998c-f4a8-402a-bf90-df3770a78685
ms.openlocfilehash: dd1f48fd584016dab740bc8a6bd05ff3b756e41b
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50486883"
---
# <a name="deleteitemstruct-structure"></a>DELETEITEMSTRUCT 구조체

`DELETEITEMSTRUCT` 구조 삭제 된 소유자가 그린 목록 상자 또는 콤보 상자 항목에서 설명 합니다.

## <a name="syntax"></a>구문

```
typedef struct tagDELETEITEMSTRUCT { /* ditms */
    UINT CtlType;
    UINT CtlID;
    UINT itemID;
    HWND hwndItem;
    UINT itemData;
} DELETEITEMSTRUCT;
```

#### <a name="parameters"></a>매개 변수

*CtlType*<br/>
ODT_LISTBOX (소유자가 그린 목록 상자) 또는 ODT_COMBOBOX (소유자가 그린 콤보 상자)를 지정합니다.

*CtlID*<br/>
목록 상자 또는 콤보 상자의 식별자를 지정 합니다.

*itemID*<br/>
목록 상자 또는 콤보 상자 제거할 항목의 인덱스를 지정 합니다.

*hwndItem*<br/>
컨트롤을 식별합니다.

*itemData*<br/>
항목에 대 한 응용 프로그램 정의 데이터를 지정합니다. 이 값은 컨트롤에 전달 된 *lParam* 목록 상자 또는 콤보 상자에 항목을 추가 하는 메시지의 매개 변수입니다.

## <a name="remarks"></a>설명

항목 목록 상자 또는 콤보 상자 또는 목록 상자나 콤보 상자 소멸 될 때 제거 되 면 Windows는 삭제 된 각 항목에 대 한 소유자 WM_DELETEITEM 메시지를 보냅니다. 합니다 *lParam* 메시지의 매개 변수는이 구조에 대 한 포인터를 포함 합니다.

## <a name="requirements"></a>요구 사항

**헤더:** atldbcli.h

## <a name="see-also"></a>참고 항목

[구조체, 스타일, 콜백 및 메시지 맵](../../mfc/reference/structures-styles-callbacks-and-message-maps.md)<br/>
[CWnd::OnDeleteItem](../../mfc/reference/cwnd-class.md#ondeleteitem)

