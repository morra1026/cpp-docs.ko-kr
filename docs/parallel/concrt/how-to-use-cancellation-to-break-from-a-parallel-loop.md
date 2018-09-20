---
title: '방법: break 취소를 사용 하 여 병렬 루프에서 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-concrt
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- writing a parallel search algorithm [Concurrency Runtime]
- parallel search algorithm, writing [Concurrency Runtime]
ms.assetid: 421cd2de-f058-465f-b890-dd8fcc0df273
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 9172132f0bdaabea9d6959a3f947d7b50d5261da
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46417334"
---
# <a name="how-to-use-cancellation-to-break-from-a-parallel-loop"></a>방법: 취소를 사용하여 병렬 루프 중단

이 예제에서는 취소를 사용하여 기본적인 병렬 검색 알고리즘을 구현하는 방법을 보여 줍니다.

## <a name="example"></a>예제

다음 예제에서는 배열에서 요소를 검색 하려면 취소를 사용 합니다. `parallel_find_any` 함수는 합니다 [concurrency:: parallel_for](reference/concurrency-namespace-functions.md#parallel_for) 알고리즘 및 [run_with_cancellation_token](reference/concurrency-namespace-functions.md#run_with_cancellation_token) 함수를 지정된 된 값을 포함 하는 위치를 검색 합니다. 병렬 루프는 값을 찾을 경우 호출 하는 [concurrency::cancellation_token_source::cancel](reference/cancellation-token-source-class.md#cancel) 이후의 작업을 취소 하는 방법입니다.

[!code-cpp[concrt-parallel-array-search#1](../../parallel/concrt/codesnippet/cpp/how-to-use-cancellation-to-break-from-a-parallel-loop_1.cpp)]

합니다 [concurrency:: parallel_for](reference/concurrency-namespace-functions.md#parallel_for) 알고리즘은 동시에 동작 합니다. 따라서 미리 결정 된 순서로 작업을 수행 하지 않습니다. 값의 여러 인스턴스를 포함 하는 경우 결과 해당 위치 중 하나일 수 있습니다.

## <a name="compiling-the-code"></a>코드 컴파일

예제 코드를 복사 하 고 Visual Studio 프로젝트에 붙여 넣습니다 또는 라는 파일에 붙여 `parallel-array-search.cpp` Visual Studio 명령 프롬프트 창에서 다음 명령을 실행 합니다.

**cl.exe /EHsc 병렬-배열-search.cpp**

## <a name="see-also"></a>참고 항목

[PPL에서의 취소](cancellation-in-the-ppl.md)<br/>
[병렬 알고리즘](../../parallel/concrt/parallel-algorithms.md)<br/>
[parallel_for 함수](reference/concurrency-namespace-functions.md#parallel_for)<br/>
[cancellation_token_source 클래스](../../parallel/concrt/reference/cancellation-token-source-class.md)
