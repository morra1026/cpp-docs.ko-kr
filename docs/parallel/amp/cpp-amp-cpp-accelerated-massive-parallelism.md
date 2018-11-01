---
title: C++ AMP(C++ Accelerated Massive Parallelism)
ms.date: 11/04/2016
helpviewer_keywords:
- C++ AMP (see C++ Accelerated Massive Parallelism)
- C++ Accelerated Massive Parallelism, getting started
ms.assetid: e27824cb-3167-409b-8c3f-a0e476d8f349
ms.openlocfilehash: f8ac71023f66868a66fb8c54a5e86678225378a1
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50613176"
---
# <a name="c-amp-c-accelerated-massive-parallelism"></a>C++ AMP(C++ Accelerated Massive Parallelism)

C + + AMP (c + + Accelerated Massive Parallelism) 일반적으로 개별 그래픽 카드의 그래픽 처리 장치 (GPU)로 존재 하는 데이터 병렬 하드웨어를 활용 하 여 c + + 코드의 실행을 가속화 합니다. C + + AMP 프로그래밍 모델에서는 다차원 배열, 인덱싱, 메모리 전송 및 바둑판식 배열을 지원 합니다. 또한 수학 함수 라이브러리가 포함 됩니다. C + + AMP 언어 확장을 사용 하 여에 CPU에서 GPU로 데이터를 이동 하는 방법을 제어할 수 있으며 다시 수 있습니다.

## <a name="related-topics"></a>관련 항목

|제목|설명|
|-----------|-----------------|
|[C++ AMP 개요](../../parallel/amp/cpp-amp-overview.md)|C + + AMP와 수학 라이브러리의 주요 기능을 설명합니다.|
|[람다, 함수 개체 및 제한 함수 사용](../../parallel/amp/using-lambdas-function-objects-and-restricted-functions.md)|에 대 한 호출에서 람다 식, 함수 개체 및 제한 함수를 사용 하는 방법에 설명 합니다 [parallel_for_each](reference/concurrency-namespace-functions-amp.md#parallel_for_each) 메서드.|
|[타일 사용](../../parallel/amp/using-tiles.md)|C + + AMP 코드를 가속화 하려면 타일을 사용 하는 방법에 설명 합니다.|
|[accelerator 및 accelerator_view 개체 사용](../../parallel/amp/using-accelerator-and-accelerator-view-objects.md)|가속기를 사용 하 여 GPU에서 코드의 실행을 사용자 지정 하는 방법에 설명 합니다.|
|[UWP 앱에서 C++ AMP 사용](../../parallel/amp/using-cpp-amp-in-windows-store-apps.md)|Windows 런타임 형식을 사용 하는 유니버설 Windows 플랫폼 (UWP) 앱에서 c + + AMP를 사용 하는 방법을 설명 합니다.|
|[그래픽(C++ AMP)](../../parallel/amp/graphics-cpp-amp.md)|C + + AMP 그래픽 라이브러리를 사용 하는 방법을 설명 합니다.|
|[연습: 매트릭스 곱](../../parallel/amp/walkthrough-matrix-multiplication.md)|C + + AMP 코드를 사용 하 고 바둑판식 매트릭스 곱하기를 보여줍니다.|
|[연습: C++ AMP 응용 프로그램 디버깅](../../parallel/amp/walkthrough-debugging-a-cpp-amp-application.md)|작성 및 큰 정수 배열을 정리 하기 위한 병렬 영역 감소를 사용 하는 응용 프로그램을 디버깅 하는 방법을 설명 합니다.|

## <a name="reference"></a>참조

[참조(C++ AMP)](../../parallel/amp/reference/reference-cpp-amp.md)<br/>
[tile_static 키워드](../../cpp/tile-static-keyword.md)<br/>
[restrict(C++ AMP)](../../cpp/restrict-cpp-amp.md)

## <a name="other-resources"></a>기타 리소스

[네이티브 코드 블로그의 병렬 프로그래밍](http://go.microsoft.com/fwlink/p/?linkid=238472)<br/>
[C + + AMP 샘플 프로젝트 다운로드](http://go.microsoft.com/fwlink/p/?linkid=248508)<br/>
[동시성 시각화 도우미를 사용 하 여 c + + AMP 코드 분석](https://blogs.msdn.microsoft.com/nativeconcurrency/2012/03/09/analyzing-c-amp-code-with-the-concurrency-visualizer/)