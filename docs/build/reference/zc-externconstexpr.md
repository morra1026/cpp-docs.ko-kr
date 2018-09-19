---
title: '/Zc: externconstexpr (extern constexpr 변수 사용) | Microsoft Docs'
ms.custom: ''
ms.date: 02/28/2018
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- /Zc:externConstexpr
dev_langs:
- C++
helpviewer_keywords:
- -Zc:externConstexpr compiler option (C++)
- extern constexpr variables (C++)
ms.assetid: 4da5e33a-2e4d-4ed2-8616-bd8f43265c27
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 34aea466a3e673c3eebb3b415d544d9299fed615
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45713143"
---
# <a name="zcexternconstexpr-enable-extern-constexpr-variables"></a>/Zc: externconstexpr (extern constexpr 변수 사용)

합니다 **/zc: externconstexpr** 컴파일러 옵션은 c + + 표준을 준수 하 고 외부 링크를 허용 하도록 컴파일러에 지시 `constexpr` 변수입니다. 기본적으로 Visual Studio 항상 제공을 `constexpr` 지정할 경우에 변수 내부 링크에는 `extern` 키워드입니다.

## <a name="syntax"></a>구문

> **/Zc:externConstexpr**[**-**]

## <a name="remarks"></a>설명

합니다 **/zc: externconstexpr** 컴파일러 옵션을 사용 하면 외부 링크를 사용 하 여 선언 된 변수를 적용할 컴파일러 `extern constexpr`합니다. 이전 버전의 Visual Studio 및 기본적으로 이거나 **/Zc:externConstexpr-** 지정 된 경우 Visual Studio 내부 링크에 적용 됩니다 `constexpr` 경우에도 변수는 `extern` 키워드를 사용 합니다. 합니다 **/zc: externconstexpr** 옵션은 Visual Studio 2017 업데이트 15.6부터 사용할 수 있습니다. 기본적으로 꺼져 있습니다. [/ permissive-](permissive-standards-conformance.md) 옵션이 사용 되지 않습니다 **/zc: externconstexpr**합니다.

헤더 파일에 선언 된 변수에 포함 되어 있으면 `extern constexpr`를 표시 해야 [__declspec (selectany)](../../cpp/selectany.md) 중복 선언과 연결 된 이진 파일의 단일 인스턴스를 병합 하기 위해. 그렇지 않으면 단일 정의 규칙의 위반에 대 한 LNK2005 예를 들어, 링커 오류가 발생할 수 있습니다.

### <a name="to-set-this-compiler-option-in-visual-studio"></a>Visual Studio에서 이 컴파일러 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.

1. 선택 된 **구성 속성** > **C/c + +** > **명령줄** 속성 페이지.

1. 추가 **/zc: externconstexpr** 하거나 **/Zc:externConstexpr-** 하는 **추가 옵션:** 창.

## <a name="see-also"></a>참고 항목

[/Zc (규칙)](../../build/reference/zc-conformance.md)
[auto 키워드](../../cpp/auto-keyword.md)