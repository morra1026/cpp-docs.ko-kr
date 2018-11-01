---
title: FILETIME 구조체
ms.date: 11/04/2016
f1_keywords:
- FILETIME
helpviewer_keywords:
- FILETIME structure [MFC]
ms.assetid: e09557e2-b6d7-4dd5-a5b9-6328bca88595
ms.openlocfilehash: f70792b83637018e707b6ee48d1b169f28d46d71
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50514935"
---
# <a name="filetime-structure"></a>FILETIME 구조체

`FILETIME` 구조는 1601 년 1 월 1 일 이후 100 나노초 간격의 수를 나타내는 64 비트 값입니다.

## <a name="syntax"></a>구문

```
typedef struct _FILETIME {
    DWORD dwLowDateTime;   /* low 32 bits */
    DWORD dwHighDateTime;  /* high 32 bits */
} FILETIME, *PFILETIME, *LPFILETIME;
```

#### <a name="parameters"></a>매개 변수

*dwLowDateTime*<br/>
낮은 파일의 32 비트를 지정합니다.

*dwHighDateTime*<br/>
높은 파일의 32 비트를 지정합니다.

## <a name="requirements"></a>요구 사항

**헤더:** windef.h

## <a name="see-also"></a>참고 항목

[구조체, 스타일, 콜백 및 메시지 맵](../../mfc/reference/structures-styles-callbacks-and-message-maps.md)<br/>
[CTime::CTime](../../atl-mfc-shared/reference/ctime-class.md#ctime)

