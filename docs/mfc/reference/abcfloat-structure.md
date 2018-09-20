---
title: ABCFLOAT 구조체 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: reference
f1_keywords:
- ABCFLOAT
dev_langs:
- C++
helpviewer_keywords:
- ABCFLOAT structure [MFC]
ms.assetid: 338e7e15-9d2c-42d0-aa80-273acfde5cc5
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 5a9bbece0773c14a4a8b545bc56209bf682e22c0
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46375416"
---
# <a name="abcfloat-structure"></a>ABCFLOAT 구조체

`ABCFLOAT` 구조 A, B 및 C 글꼴 문자의 너비를 포함 합니다.

## <a name="syntax"></a>구문

```
typedef struct _ABCFLOAT { /* abcf */
    FLOAT abcfA;
    FLOAT abcfB;
    FLOAT abcfC;
} ABCFLOAT;
```

#### <a name="parameters"></a>매개 변수

*abcfA*<br/>
문자는 간격을 지정합니다. 간격에는 문자 모양 그리기 전에 현재 위치에 추가할 거리입니다.

*abcfB*<br/>
문자 B 간격을 지정합니다. B 간격에는 문자 모양이 그려지는 부분의 너비입니다.

*abcfC*<br/>
문자 C 간격을 지정합니다. C 간격에는 문자 모양의 오른쪽에 공백 수 있도록 현재 위치에 추가할 거리입니다.

## <a name="remarks"></a>설명

A, B 및 C 너비 글꼴의 기준선을 따라 측정 됩니다. 문자의 문자 증가값 (총 너비) A, B와 C 공간의 합계가 표시 됩니다. A 또는 C 공간 underhangs 또는 돌출부 나타내기 위해 음수일 수 있습니다.

## <a name="requirements"></a>요구 사항

**헤더:** wingdi.h

## <a name="see-also"></a>참고 항목

[구조체, 스타일, 콜백 및 메시지 맵](../../mfc/reference/structures-styles-callbacks-and-message-maps.md)<br/>
[CDC::GetCharABCWidths](../../mfc/reference/cdc-class.md#getcharabcwidths)

