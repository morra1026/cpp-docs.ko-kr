---
title: SYSTEMTIME 구조체
ms.date: 11/04/2016
f1_keywords:
- SYSTEMTIME
helpviewer_keywords:
- SYSTEMTIME structure [MFC]
ms.assetid: 9aaef4d6-de79-4fa1-8158-86b245ef5bff
ms.openlocfilehash: b46482a9f4eb0165b72d74cb7d69e96e2a15e953
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50559051"
---
# <a name="systemtime-structure"></a>SYSTEMTIME 구조체

`SYSTEMTIME` 구조는 날짜 및 시간을 월, 일, 연도, 요일, 시간, 분, 초 및 밀리초에 대 한 개별 멤버를 사용 하 여 나타냅니다.

## <a name="syntax"></a>구문

```
typedef struct _SYSTEMTIME {
    WORD wYear;
    WORD wMonth;
    WORD wDayOfWeek;
    WORD wDay;
    WORD wHour;
    WORD wMinute;
    WORD wSecond;
    WORD wMilliseconds;
} SYSTEMTIME;
```

#### <a name="parameters"></a>매개 변수

*wYear*<br/>
현재 연도입니다.

*wMonth*<br/>
현재 월입니다. 월은 1입니다.

*wDayOfWeek*<br/>
주간의 당일 일요일은 0, 월요일은 1입니다.

*wDay*<br/>
해당 월의 현재 날짜입니다.

*wHour*<br/>
현재 시간입니다.

*wMinute*<br/>
현재 분입니다.

*wSecond*<br/>
현재 초입니다.

*wMilliseconds*<br/>
현재 밀리초입니다.

## <a name="example"></a>예제

[!code-cpp[NVC_MFC_Utilities#39](../../mfc/codesnippet/cpp/systemtime-structure1_1.cpp)]

## <a name="requirements"></a>요구 사항

**헤더:** winbase.h

## <a name="see-also"></a>참고 항목

[구조체, 스타일, 콜백 및 메시지 맵](../../mfc/reference/structures-styles-callbacks-and-message-maps.md)<br/>
[CTime::CTime](../../atl-mfc-shared/reference/ctime-class.md#ctime)

