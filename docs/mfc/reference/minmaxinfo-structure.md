---
title: MINMAXINFO 구조체
ms.date: 11/04/2016
f1_keywords:
- MINMAXINFO
helpviewer_keywords:
- MINMAXINFO structure [MFC]
ms.assetid: be6fb578-f98a-4581-9ada-be9df308ed2f
ms.openlocfilehash: 11f55b1756623626769e21c006543b6993607b08
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50517847"
---
# <a name="minmaxinfo-structure"></a>MINMAXINFO 구조체

`MINMAXINFO` 구조 상태의 최대화 된 창의 크기 및 위치 최소 및 최대 추적 크기에 대 한 정보가 들어 있습니다.

## <a name="syntax"></a>구문

```
typedef struct tagMINMAXINFO {
    POINT ptReserved;
    POINT ptMaxSize;
    POINT ptMaxPosition;
    POINT ptMinTrackSize;
    POINT ptMaxTrackSize;
} MINMAXINFO;
```

#### <a name="parameters"></a>매개 변수

*ptReserved*<br/>
내부용으로 예약됩니다.

*ptMaxSize*<br/>
최대화 된 상태로 너비 (point.x) 및 창 최대화 (point.y) 높이 지정합니다.

*ptMaxPosition*<br/>
최대화 된 창 (point.x) 왼쪽의 위치와 상태의 최대화 된 창 (point.y)의 위쪽 위치를 지정합니다.

*ptMinTrackSize*<br/>
최소 추적 너비 (point.x) 및 최소 추적 창의 높이 (point.y)를 지정 합니다.

*ptMaxTrackSize*<br/>
최대 너비 (point.x) 추적 및 추적 창의 높이 (point.y) 최대값을 지정 합니다.

## <a name="requirements"></a>요구 사항

**헤더:** winuser.h

## <a name="see-also"></a>참고 항목

[구조체, 스타일, 콜백 및 메시지 맵](../../mfc/reference/structures-styles-callbacks-and-message-maps.md)<br/>
[CWnd::OnGetMinMaxInfo](../../mfc/reference/cwnd-class.md#ongetminmaxinfo)

