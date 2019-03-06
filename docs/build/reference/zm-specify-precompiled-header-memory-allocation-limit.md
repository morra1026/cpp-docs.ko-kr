---
title: /Zm(미리 컴파일된 헤더 메모리 할당 제한 지정)
ms.date: 11/04/2016
f1_keywords:
- /zm
helpviewer_keywords:
- PCH files, memory allocation limit
- Zm compiler option [C++]
- /Zm compiler option [C++]
- precompiled header files, memory allocation limit
- Specify Precompiled Header Memory Allocation Limit compiler option
- cl.exe compiler, memory allocation limit
- .pch files, memory allocation limit
- memory allocation, Memory Allocation Limit compiler option
- -Zm compiler option [C++]
ms.assetid: 94c77d5e-6672-46a7-92e0-3f69e277727d
ms.openlocfilehash: d0f79ed1b38401abbc65898193f2305bd432bb28
ms.sourcegitcommit: bff17488ac5538b8eaac57156a4d6f06b37d6b7f
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57419922"
---
# <a name="zm-specify-precompiled-header-memory-allocation-limit"></a>/Zm(미리 컴파일된 헤더 메모리 할당 제한 지정)

미리 컴파일된 헤더를 생성하기 위해 컴파일러에서 할당하는 메모리의 양을 결정합니다.

## <a name="syntax"></a>구문

```
/Zmfactor
```

## <a name="arguments"></a>인수

*factor*<br/>
미리 컴파일된 헤더를 생성하기 위해 컴파일러에서 사용하는 메모리의 양을 결정하는 배율 인수입니다.

합니다 *비율* 인수는 컴파일러에 정의 된 작업 버퍼의 기본 크기의 백분율입니다. 기본값인 *비율* 100 (퍼센트) 이지만 크거나 작게 지정할 수 있습니다.

## <a name="remarks"></a>설명

이전 버전의 Visual C++의 컴파일러에서는 각각 제한이 있는 별개의 몇 가지 힙을 사용했습니다. 그러나 지금은 컴파일러에서 필요에 따라 동적으로 힙의 크기를 전체 힙 크기 한계까지 늘리기 때문에 미리 컴파일된 헤더를 생성하기 위해 고정 크기 버퍼만 필요합니다. 따라서 합니다 **/Zm** 컴파일러 옵션은 거의 필요 하지 않습니다.

컴파일러의 힙 공간이 부족 하 고 내보내는 경우 합니다 [C1060](../../error-messages/compiler-errors-1/fatal-error-c1060.md) 사용 하는 경우 오류 메시지를 **/Zm** 컴파일러 옵션을 너무 많은 메모리를 예약한 것일 수 있습니다. 제거해 합니다 **/Zm** 옵션입니다. 컴파일러에서는 [C1076](../../error-messages/compiler-errors-1/fatal-error-c1076.md) 오류 메시지가 발생 하면 [C3859](../../error-messages/compiler-errors-2/compiler-error-c3859.md) 메시지를 지정 합니다 *비율* 를사용하여컴파일할때사용하는인수 **/Zm** 컴파일러 옵션입니다.

다음 표는 하는 방법을 *비율* 인수 기본 미리 컴파일된 헤더 버퍼의 크기를 75mb로 가정할 경우 메모리 할당 제한에 영향을 줍니다.

|값 *비율*|메모리 할당 제한|
|-----------------------|-----------------------------|
|10|7.5 MB|
|100|75 MB|
|200|150MB|
|1000|750MB|
|2000|1500 (MB)|

## <a name="other-ways-to-set-the-memory-allocation-limit"></a>메모리 할당 제한을 설정하는 기타 방법

#### <a name="to-set-the-zm-compiler-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 /Zm 컴파일러 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. 탐색 창에서 선택 **구성 속성**, **C/c + +** 하십시오 **명령줄**합니다.

1. 입력 된 **/Zm** 컴파일러 옵션을 **추가 옵션** 상자.

#### <a name="to-set-the-zm-compiler-option-programmatically"></a>프로그래밍 방식으로 /Zm 컴파일러 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions%2A>을 참조하세요.

## <a name="see-also"></a>참고자료

[컴파일러 옵션](../../build/reference/compiler-options.md)<br/>
[컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md)
