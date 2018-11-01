---
title: POINT 구조체
ms.date: 10/12/2018
f1_keywords:
- POINT
- LPPOINT
helpviewer_keywords:
- LPPOINT structure [MFC]
- POINT structure [MFC]
ms.assetid: 965736d8-4e53-41b6-9b8b-6961992dd21f
ms.openlocfilehash: c53f250b714c66e74a12432b879cbc4bcc1fd88d
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50646903"
---
# <a name="point-structure"></a>POINT 구조체

합니다 `POINT` 구조 정의 x*-* 및 점의 y-좌표입니다.

## <a name="syntax"></a>구문

```
typedef struct tagPOINT {
    LONG x;
    LONG y;
} POINT;
```

#### <a name="parameters"></a>매개 변수

*x*<br/>
점의 x 좌표를 지정합니다.

*y*<br/>
점의 y 좌표를 지정합니다.

## <a name="example"></a>예제

[!code-cpp[NVC_MFC_Utilities#37](../../mfc/codesnippet/cpp/point-structure1_1.cpp)]

## <a name="requirements"></a>요구 사항

**헤더:** windef.h

## <a name="see-also"></a>참고 항목

[구조체, 스타일, 콜백 및 메시지 맵](../../mfc/reference/structures-styles-callbacks-and-message-maps.md)<br/>
[CPoint 클래스](../../atl-mfc-shared/reference/cpoint-class.md)
