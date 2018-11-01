---
title: 와일드카드 식
ms.date: 11/04/2016
f1_keywords:
- _setargv
helpviewer_keywords:
- asterisk wildcard
- _setargv function
- command line [C++], processing arguments
- command line [C++], wildcards
- command-line wildcards
- question mark, wildcard
ms.assetid: 1a543398-607b-4404-93d1-45d290bde638
ms.openlocfilehash: 2d495f94f2e3fb7b88d235edc7b98f8e90775393
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50507435"
---
# <a name="wildcard-expansion"></a>와일드카드 식

## <a name="microsoft-specific"></a>Microsoft 전용

명령줄에서 파일 이름과 경로 인수를 지정하기 위해 와일드카드, 즉 물음표(?)와 별표(*)를 사용할 수 있습니다.

명령줄 인수는 호출 루틴에 의해 처리 됩니다 `_setargv` (또는 `_wsetargv` 와이드 문자 환경에서)에서 별도 문자열로 와일드 카드 확장 하지는 기본적으로는 `argv` 문자열 배열입니다. 와일드 카드 확장 사용에 대 한 자세한 내용은 참조 [와일드 카드 인수 확장명](../c-language/expanding-wildcard-arguments.md)합니다.

**Microsoft 전용 종료**

## <a name="see-also"></a>참고자료

[main: 프로그램 시작](../cpp/main-program-startup.md)