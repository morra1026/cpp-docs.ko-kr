---
title: RECT 구조체 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: reference
f1_keywords:
- LPRECT
- RECT
dev_langs:
- C++
helpviewer_keywords:
- RECT structure [MFC]
- LPRECT structure [MFC]
ms.assetid: 1b3160de-64e9-40d1-89eb-af3e0fd6acf0
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: eae2b248f4aa4586bf6453dcc37b521387327d25
ms.sourcegitcommit: 3f4e92266737ecb70507871e87dc8e2965ad7e04
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/15/2018
ms.locfileid: "49334570"
---
# <a name="rect-structure"></a>RECT 구조체

`RECT` 구조체는 사각형의 왼쪽 위 및 오른쪽 아래 모퉁이의 좌표를 정의합니다.

## <a name="syntax"></a>구문

```
typedef struct tagRECT {
    LONG left;
    LONG top;
    LONG right;
    LONG bottom;
} RECT;
```

## <a name="members"></a>멤버

`left`<br/>
사각형의 왼쪽 위 모퉁이의 x좌표를 지정합니다.

`top`<br/>
사각형의 왼쪽 위 모퉁이의 y좌표를 지정합니다.

`right`<br/>
사각형의 오른쪽 아래 모퉁이의 x좌표를 지정합니다.

`bottom`<br/>
사각형의 오른쪽 아래 모퉁이의 y좌표를 지정합니다.

## <a name="example"></a>예제

[!code-cpp[NVC_MFC_Utilities#38](../../mfc/codesnippet/cpp/rect-structure1_1.cpp)]

## <a name="requirements"></a>요구 사항

**헤더:** windef.h

## <a name="see-also"></a>참고 항목

[구조체, 스타일, 콜백 및 메시지 맵](../../mfc/reference/structures-styles-callbacks-and-message-maps.md)<br/>
[CRect 클래스](../../atl-mfc-shared/reference/crect-class.md)
