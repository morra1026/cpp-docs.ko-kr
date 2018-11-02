---
title: '방법: 정기적으로 메시지 보내기'
ms.date: 11/04/2016
helpviewer_keywords:
- timer class, example
- sending messages at regular intervals [Concurrency Runtime]
ms.assetid: 4b60ea6c-97c8-4d69-9f7b-ad79f3548026
ms.openlocfilehash: 05777b0c00f587f588a50733d5113d9a7362d247
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50549619"
---
# <a name="how-to-send-a-message-at-a-regular-interval"></a>방법: 정기적으로 메시지 보내기

이 예제에서는 동시성을 사용 하는 방법을 보여 줍니다::[timer 클래스](../../parallel/concrt/reference/timer-class.md) 일정 한 간격으로 메시지를 보내려고 합니다.

## <a name="example"></a>예제

다음 예제에서는 `timer` 시간이 오래 걸리는 작업을 하는 동안 진행률을 보고 하는 개체입니다. 이 예제에서는 연결 된 `timer` 개체를 [concurrency:: call](../../parallel/concrt/reference/call-class.md) 개체입니다. `call` 일정 한 간격으로 콘솔에 진행률 표시기를 인쇄 하는 개체입니다. 합니다 [concurrency::timer::start](reference/timer-class.md#start) 메서드는 별도 컨텍스트에서 타이머를 실행 합니다. 합니다 `perform_lengthy_operation` 함수 호출을 [concurrency:: wait](reference/concurrency-namespace-functions.md#wait) 시간이 오래 걸리는 작업을 시뮬레이션 하는 주 컨텍스트에서 함수입니다.

[!code-cpp[concrt-report-progress#1](../../parallel/concrt/codesnippet/cpp/how-to-send-a-message-at-a-regular-interval_1.cpp)]

이 예제는 다음 예제 출력을 생성합니다.

```Output
Performing a lengthy operation..........done.
```

## <a name="compiling-the-code"></a>코드 컴파일

예제 코드를 복사 하 고 Visual Studio 프로젝트에 붙여 넣습니다 또는 라는 파일에 붙여 `report-progress.cpp` Visual Studio 명령 프롬프트 창에서 다음 명령을 실행 합니다.

**cl.exe /EHsc report-progress.cpp**

## <a name="see-also"></a>참고 항목

[비동기 에이전트 라이브러리](../../parallel/concrt/asynchronous-agents-library.md)<br/>
[비동기 메시지 블록](../../parallel/concrt/asynchronous-message-blocks.md)<br/>
[메시지 전달 함수](../../parallel/concrt/message-passing-functions.md)
