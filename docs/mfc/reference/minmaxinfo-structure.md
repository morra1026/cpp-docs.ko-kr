---
title: MINMAXINFO 구조체 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: reference
f1_keywords:
- MINMAXINFO
dev_langs:
- C++
helpviewer_keywords:
- MINMAXINFO structure [MFC]
ms.assetid: be6fb578-f98a-4581-9ada-be9df308ed2f
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: b63589edbe47aa09b8a6be92b5b7eb7e29077c96
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46402293"
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

