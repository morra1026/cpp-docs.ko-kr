---
title: CMFCBaseToolBar 클래스
ms.date: 11/04/2016
f1_keywords:
- CMFCBaseToolBar
- AFXBASETOOLBAR/CMFCBaseToolBar
- AFXBASETOOLBAR/CMFCBaseToolBar::GetDockingMode
- AFXBASETOOLBAR/CMFCBaseToolBar::GetMinSize
- AFXBASETOOLBAR/CMFCBaseToolBar::OnAfterChangeParent
helpviewer_keywords:
- CMFCBaseToolBar [MFC], GetDockingMode
- CMFCBaseToolBar [MFC], GetMinSize
- CMFCBaseToolBar [MFC], OnAfterChangeParent
ms.assetid: 5d79206d-55e4-46f8-b1b8-042e34d7f9da
ms.openlocfilehash: 84756eb177fcec1981f3f2ed018d57eb27df9823
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50523706"
---
# <a name="cmfcbasetoolbar-class"></a>CMFCBaseToolBar 클래스

도구 모음에 대 한 기본 클래스입니다.

## <a name="syntax"></a>구문

```
class CMFCBaseToolBar : public CPane
```

## <a name="members"></a>멤버

### <a name="public-constructors"></a>Public 생성자

|이름|설명|
|----------|-----------------|
|`CMFCBaseToolBar::CMFCBaseToolBar`|기본 생성자입니다.|
|`CMFCBaseToolBar::~CMFCBaseToolBar`|소멸자|

### <a name="public-methods"></a>Public 메서드

|이름|설명|
|----------|-----------------|
|`CMFCBaseToolBar::CreateObject`|프레임워크에서 이 클래스 형식의 동적 인스턴스를 만드는 데 사용합니다.|
|[CMFCBaseToolBar::GetDockingMode](#getdockingmode)|도킹 모드를 반환합니다. (재정의 [cbasepane:: Getdockingmode](../../mfc/reference/cbasepane-class.md#getdockingmode).)|
|[CMFCBaseToolBar::GetMinSize](#getminsize)|도구 모음의 최소 크기를 반환합니다. (재정의 [CPane::GetMinSize](../../mfc/reference/cpane-class.md#getminsize).)|
|[CMFCBaseToolBar::OnAfterChangeParent](#onafterchangeparent)|창의 부모 변경 된 후 프레임 워크에서 호출 됩니다. (재정의 [CBasePane::OnAfterChangeParent](../../mfc/reference/cbasepane-class.md#onafterchangeparent).)|

## <a name="inheritance-hierarchy"></a>상속 계층

[CObject](../../mfc/reference/cobject-class.md)

[CCmdTarget](../../mfc/reference/ccmdtarget-class.md)

[CWnd](../../mfc/reference/cwnd-class.md)

[CBasePane](../../mfc/reference/cbasepane-class.md)

[CPane](../../mfc/reference/cpane-class.md)

[CMFCBaseToolBar](../../mfc/reference/cmfcbasetoolbar-class.md)

## <a name="requirements"></a>요구 사항

**헤더:** afxbasetoolbar.h

##  <a name="getdockingmode"></a>  CMFCBaseToolBar::GetDockingMode

도킹 모드를 반환합니다.

```
virtual AFX_DOCK_TYPE GetDockingMode() const;
```

### <a name="return-value"></a>반환 값

도킹 모드입니다.

##  <a name="getminsize"></a>  CMFCBaseToolBar::GetMinSize

도구 모음의 최소 크기를 반환합니다.

```
virtual void GetMinSize(CSize& size) const;
```

### <a name="parameters"></a>매개 변수

*size*<br/>
[out] 도구 모음의 최소 크기입니다.

##  <a name="onafterchangeparent"></a>  CMFCBaseToolBar::OnAfterChangeParent

창의 부모 변경 된 후 프레임 워크에서 호출 됩니다.

```
virtual void OnAfterChangeParent(CWnd* pWndOldParent);
```

### <a name="parameters"></a>매개 변수

*pWndOldParent*<br/>
[in] 이전 부모 창에 대 한 포인터입니다.

## <a name="see-also"></a>참고 항목

[계층 구조 차트](../../mfc/hierarchy-chart.md)<br/>
[클래스](../../mfc/reference/mfc-classes.md)
