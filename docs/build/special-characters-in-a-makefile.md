---
title: 메이크파일의 특수 문자
ms.date: 11/04/2016
helpviewer_keywords:
- NMAKE program, special characters
- makefiles, special characters
- special characters, in NMAKE macros
- macros, special characters
ms.assetid: 92c34ab5-ca6b-4fc0-bcf4-3172eaeda9f0
ms.openlocfilehash: 18fa83fcfd0c70ac4e8b9bf5be08ac1922998ecb
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50443732"
---
# <a name="special-characters-in-a-makefile"></a>메이크파일의 특수 문자

NMAKE 특수 문자를 리터럴 문자로 사용 하려면 앞에 캐럿 (^)를 배치 합니다. NMAKE 다른 문자 앞에 있는 캐럿을 무시 합니다. 특수 문자는 다음과 같습니다.

`:  ;  #  (  )  $  ^  \  {  }  !  @  —`

따옴표 붙은 문자열 안에 캐럿 (^)는 캐럿 리터럴 문자로 처리 됩니다. 줄의 끝에 캐럿 매크로 문자열에 리터럴 줄 바꿈 문자를 삽입합니다.

매크로, 백슬래시 (\\) 뒤에 줄 바꿈으로 문자가 공백으로 바뀝니다.

명령에서 백분율 기호 (%)는 파일 지정자를 사용 합니다. 명령에서 문자 그대로 %를 나타내기 위해 하나 대신 두 개의 백분율 기호 (%)을 지정 합니다. NMAKE 다른 상황에서는 단일 % 문자 그대로 해석 하지만 항상 double 값을 해석 % % 단일 %로 합니다. 따라서 리터럴을 나타내는 % %, 하거나 세 백분율 기호를 지정 합니다. %%%, 또는 네 개의 백분율 기호를 %%%.

명령에서 리터럴 문자로 달러 기호 ($)를 사용 하려면 두 개의 달러 기호 ($$)를 지정 합니다. 다른 상황에서는이 방법을 사용할 수도 있습니다는 ^ $ 작동 합니다.

## <a name="see-also"></a>참고 항목

[메이크파일의 내용](../build/contents-of-a-makefile.md)