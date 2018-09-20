---
title: '방법: call 및 transformer 클래스에 작업 함수 제공 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-concrt
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- call class, example
- using the transformer class [Concurrency Runtime]
- using the call class [Concurrency Runtime]
ms.assetid: df715ce4-8507-41ca-b204-636d11707a73
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 3102947009780f6f4e735b70506c5b2dc02f416b
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46438966"
---
# <a name="how-to-provide-work-functions-to-the-call-and-transformer-classes"></a>방법: call 및 transformer 클래스에 작업 함수 제공

이 항목에서는 여러 가지 방법으로 작업 함수를 제공 하는 [concurrency:: call](../../parallel/concrt/reference/call-class.md) 하 고 [concurrency:: transformer](../../parallel/concrt/reference/transformer-class.md) 클래스.

첫 번째 예제에서는 람다 식을 전달 하는 방법을 보여 줍니다는 `call` 개체입니다. 두 번째 예제에는 함수 개체에 전달 하는 방법을 보여 줍니다는 `call` 개체입니다. 세 번째 예제에서는 클래스 메서드를 바인딩하는 방법을 보여 줍니다는 `call` 개체입니다.

이 항목의 모든 예제에서는 이해를 돕기는 `call` 클래스입니다. 사용 하는 예는 `transformer` 클래스를 참조 하십시오 [방법: 데이터 파이프라인에서 transformer 사용](../../parallel/concrt/how-to-use-transformer-in-a-data-pipeline.md)합니다.

## <a name="example"></a>예제

다음 예제에서는 사용 하는 일반적인 방법은 `call` 클래스입니다. 이 예제에서는 람다 함수에 전달 된 `call` 생성자입니다.

[!code-cpp[concrt-call-lambda#1](../../parallel/concrt/codesnippet/cpp/how-to-provide-work-functions-to-the-call-and-transformer-classes_1.cpp)]

이 예제의 결과는 다음과 같습니다.

```Output
13 squared is 169.
```

## <a name="example"></a>예제

다음 예제에서는 이전 예제와 유사를 사용 하 여 `call` 함수 개체 (functor)와 함께 클래스.

[!code-cpp[concrt-call-functor#1](../../parallel/concrt/codesnippet/cpp/how-to-provide-work-functions-to-the-call-and-transformer-classes_2.cpp)]

## <a name="example"></a>예제

다음 예제에서는 이전 예제와 유사 합니다 사용 한다는 점을 제외 하 고는 [std::bind1st](../../standard-library/functional-functions.md#bind1st) 및 [std::mem_fun](../../standard-library/functional-functions.md#mem_fun) 바인딩하는 함수를 `call` 클래스 메서드는 개체입니다.

바인딩할 경우이 기술을 사용 하 여는 `call` 또는 `transformer` 함수 호출 연산자 대신 특정 클래스 메서드에 개체 `operator()`합니다.

[!code-cpp[concrt-call-method#1](../../parallel/concrt/codesnippet/cpp/how-to-provide-work-functions-to-the-call-and-transformer-classes_3.cpp)]

결과 할당할 수도 있습니다는 `bind1st` 함수를 [std:: function](../../standard-library/function-class.md) 개체 또는 사용 하 여는 `auto` 키워드를 다음 예제에서와 같이 합니다.

[!code-cpp[concrt-call-method#2](../../parallel/concrt/codesnippet/cpp/how-to-provide-work-functions-to-the-call-and-transformer-classes_4.cpp)]

## <a name="compiling-the-code"></a>코드 컴파일

예제 코드를 복사 하 고 Visual Studio 프로젝트에 붙여 넣습니다 또는 라는 파일에 붙여 `call.cpp` Visual Studio 명령 프롬프트 창에서 다음 명령을 실행 합니다.

**cl.exe /EHsc call.cpp**

## <a name="see-also"></a>참고 항목

[비동기 에이전트 라이브러리](../../parallel/concrt/asynchronous-agents-library.md)<br/>
[비동기 메시지 블록](../../parallel/concrt/asynchronous-message-blocks.md)<br/>
[방법: 데이터 파이프라인에서 transformer 사용](../../parallel/concrt/how-to-use-transformer-in-a-data-pipeline.md)<br/>
[call 클래스](../../parallel/concrt/reference/call-class.md)<br/>
[transformer 클래스](../../parallel/concrt/reference/transformer-class.md)
