---
title: 'WM_ 메시지 처리기: -C'
ms.date: 11/04/2016
f1_keywords:
- ON_WM_CREATE
- ON_WM_COMPACTING
- ON_WM_CHARTOITEM
- ON_WM_ASKCBFORMATNAME
- ON_WM_CTLCOLOR
- ON_WM_COMPAREITEM
- ON_WM_CHILDACTIVATE
- ON_WM_CONTEXTMENU
- ON_WM_ACTIVATE
- ON_WM_CANCELMODE
- ON_WM_CLOSE
- ON_WM_CAPTURECHANGED
- ON_WM_ACTIVATEAPP
- ON_WM_CHAR
- ON_WM_CHANGECBCHAIN
helpviewer_keywords:
- ON_WM_COMPACTING [MFC]
- ON_WM_COMPAREITEM [MFC]
- ON_WM_CLOSE [MFC]
- ON_WM_CTLCOLOR [MFC]
- ON_WM_CHAR [MFC]
- ON_WM_CAPTURECHANGED [MFC]
- ON_WM_CHARTOITEM [MFC]
- ON_WM_CREATE [MFC]
- ON_WM_ACTIVATE [MFC]
- ON_WM_CONTEXTMENU [MFC]
- ON_WM_CANCELMODE [MFC]
- ON_WM_ASKCBFORMATNAME [MFC]
- ON_WM_CHILDACTIVATE [MFC]
- WM_ messages [MFC]
- ON_WM_ACTIVATEAPP [MFC]
- ON_WM_CHANGECBCHAIN
ms.assetid: 4e315896-d646-4b87-b0ab-41a4a753b045
ms.openlocfilehash: 08221e7569a8b4c4f4e8decba410bd1fe40f04d7
ms.sourcegitcommit: c3093251193944840e3d0a068ecc30e6449624ba
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2019
ms.locfileid: "57266031"
---
# <a name="wm-message-handlers-a---c"></a>WM_ 메시지 처리기: -C

왼쪽에 있는 다음 맵 항목은 오른쪽에 있는 함수 프로토타입과 일치합니다.

|맵 항목|함수 프로토타입|
|---------------|------------------------|
|ON_WM_ACTIVATE()|afx_msg void [OnActivate](../../mfc/reference/cwnd-class.md#onactivate)(UINT, CWnd\*, BOOL);|
|ON_WM_ACTIVATEAPP()|afx_msg void [OnActivateApp](../../mfc/reference/cwnd-class.md#onactivateapp)(BOOL, DWORD);|
|ON_WM_APPCOMMAND()|afx_msg void [OnAppCommand](../../mfc/reference/cwnd-class.md#onappcommand)(CWnd\*, UINT, UINT, UINT);|
|ON_WM_ASKCBFORMATNAME()|afx_msg void [OnAskCbFormatName](../../mfc/reference/cwnd-class.md#onaskcbformatname)(UINT, LPSTR);|
|ON_WM_CANCELMODE()|afx_msg void [OnCancelMode](../../mfc/reference/cwnd-class.md#oncancelmode)();|
|ON_WM_CAPTURECHANGED()|afx_msg void [OnCaptureChanged](../../mfc/reference/cwnd-class.md#oncapturechanged)(CWnd\*);|
|ON_WM_CHANGECBCHAIN()|afx_msg void [OnChangeCbChain](../../mfc/reference/cwnd-class.md#onchangecbchain)(HWND, HWND)입니다.|
|ON_WM_CHAR()|afx_msg void [OnChar](../../mfc/reference/cwnd-class.md#onchar)(UINT, UINT, UINT);|
|ON_WM_CHARTOITEM()|afx_msg int [OnCharToItem](../../mfc/reference/cwnd-class.md#onchartoitem)(UINT, CWnd\*, UINT);|
|ON_WM_CHILDACTIVATE()|afx_msg void [OnChildActivate](../../mfc/reference/cwnd-class.md#onchildactivate)();|
|ON_WM_CLIPBOARDUPDATE()|afx_msg void [OnClipboardUpdate](../../mfc/reference/cwnd-class.md#onclipboardupdate)();|
|ON_WM_CLOSE()|afx_msg void [OnClose](../../mfc/reference/cwnd-class.md#onclose)();|
|ON_WM_COMPACTING()|afx_msg void [OnCompacting](../../mfc/reference/cwnd-class.md#oncompacting)(UINT);|
|ON_WM_COMPAREITEM()|afx_msg int [OnCompareItem](../../mfc/reference/cwnd-class.md#oncompareitem)(LPCOMPAREITEMSTRUCT);|
|ON_WM_CONTEXTMENU()|afx_msg void [OnContextMenu](../../mfc/reference/cwnd-class.md#oncontextmenu)(CWnd\*, CPoint);|
|ON_WM_COPYDATA()|BOOL afx_msg [OnCopyData](../../mfc/reference/cwnd-class.md#oncopydata)(CWnd\* pWnd, COPYDATASTRUCT\* pCopyDataStruct);|
|ON_WM_CREATE()|afx_msg int [OnCreate](../../mfc/reference/cwnd-class.md#oncreate)(LPCREATESTRUCT);|
|ON_WM_CTLCOLOR()|afx_msg HBRUSH [OnCtlColor](../../mfc/reference/cwnd-class.md#onctlcolor)(CDC\*, CWnd\*, UINT);|

## <a name="see-also"></a>참고자료

[메시지 맵](../../mfc/reference/message-maps-mfc.md)<br/>
[WM_ 메시지 처리기](../../mfc/reference/handlers-for-wm-messages.md)
