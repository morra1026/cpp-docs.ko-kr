---
title: 이벤트 처리 전역 함수
ms.date: 11/04/2016
f1_keywords:
- atlbase/ATL::AtlWaitWithMessageLoop
helpviewer_keywords:
- event handling, global functions
- global functions, event handling
ms.assetid: fd674470-3def-47c3-be1c-894fa85f13e8
ms.openlocfilehash: bb109c63b497420ad6e797cd8e0b366ce4dc0475
ms.sourcegitcommit: c3093251193944840e3d0a068ecc30e6449624ba
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2019
ms.locfileid: "57292226"
---
# <a name="event-handling-global-functions"></a>이벤트 처리 전역 함수

이 함수는 이벤트 처리기를 제공합니다.

> [!IMPORTANT]
>  다음 표에 나열 된 함수는 Windows 런타임에서 실행 되는 응용 프로그램에서 사용할 수 없습니다.

|||
|-|-|
|[AtlWaitWithMessageLoop](#atlwaitwithmessageloop)|필요에 따라 창 메시지를 디스패치 개체에 신호를 기다립니다.|

## <a name="requirements"></a>요구 사항

**헤더:** atlbase.h

##  <a name="atlwaitwithmessageloop"></a>  AtlWaitWithMessageLoop

필요에 따라 창 메시지를 디스패치하는 중에 개체가 신호를 받는 동안 대기합니다.

> [!IMPORTANT]
>  이 함수는 Windows 런타임에서 실행 되는 응용 프로그램에서 사용할 수 없습니다.

```
BOOL AtlWaitWithMessageLoop(HANDLE hEvent);
```

### <a name="parameters"></a>매개 변수

*hEvent*<br/>
[in] 대기할 개체의 핸들입니다.

### <a name="return-value"></a>반환 값

개체가 신호를 받은 경우 TRUE를 반환 합니다.

### <a name="remarks"></a>설명

개체의 이벤트를 발생 하 고 발생 하 고 알림을 받을 때까지 대기 하 긴 하지만 창 메시지를 대기 하는 동안 디스패치할 수를 허용 하는 경우에 유용 합니다.

## <a name="see-also"></a>참고자료

[함수](../../atl/reference/atl-functions.md)
