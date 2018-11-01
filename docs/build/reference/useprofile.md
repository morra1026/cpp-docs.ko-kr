---
title: /USEPROFILE (LTCG 사용 하 여 사용 하 여 PGO 데이터)
ms.date: 03/14/2018
f1_keywords:
- USEPROFILE
ms.openlocfilehash: 4b780bed3b92b874f2bf18fb0235e8e2baf95ae9
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50550633"
---
# <a name="useprofile-run-pgo-in-thread-safe-mode"></a>/USEPROFILE (스레드 안전 모드에서 PGO 실행)

와 함께이 링커 옵션 [/LTCG (링크 타임 코드 생성](ltcg-link-time-code-generation.md) 프로필 기반 최적화 (PGO) 학습 데이터를 사용 하 여 작성 하도록 링커에 지시 합니다.

## <a name="syntax"></a>구문

> **/USEPROFILE**[**:**{**AGGRESSIVE**|**PGD=**_filename_}]

### <a name="arguments"></a>인수

**적극적인**<br/>
이 인수는 최적화 된 코드를 생성 하는 동안 적극적으로 속도 최적화를 사용 해야 함을 지정 합니다.

**PGD**=*파일 이름*<br/>
.pgd 파일의 기본 파일 이름을 지정합니다. 기본적으로 링커는.pgd 확장명을 가진 기본 실행 파일 이름을 사용합니다.

## <a name="remarks"></a>설명

합니다 **/USEPROFILE** 링커 옵션은 함께 사용 됩니다 **/LTCG** 를 생성 하거나 PGO 교육 데이터를 기반으로 하는 최적화 된 빌드를 업데이트 합니다. 에 해당 하는 사용 되지 않는 것 **/ltcg: pgupdate** 하 고 **/ltcg: pgoptimize** 옵션입니다.

선택적 **공격적인** 인수 속도 최적화 하려고 크기 관련 추론을 사용 하지 않도록 설정 합니다. 이 경우 대체로 프로그램 실행 파일의 크기가 증가 하 고 결과 속도 늘릴 수 있습니다 하는 최적화 될 수 있습니다. 프로 파일링 하 고 사용 하 여 사용 하지 않는 한 결과 비교 해야 **공격적인**합니다. 이 인수를 명시적으로; 지정 해야 기본적으로 사용 되지 않습니다.

합니다 **PGD** 인수를 사용 하려면에서 같이 학습 데이터가.pgd 파일의 선택적 이름을 지정 [/GENPROFILE 또는 /FASTGENPROFILE](genprofile-fastgenprofile-generate-profiling-instrumented-build.md)합니다. 에 해당 하는 사용 되지 않는 것 **/PGD** 전환 합니다. 기본적으로 없는 경우 또는 *filename* 지정 된 실행 파일이 사용 되는 동일한 기본 이름을 가진.pgd 파일을 합니다.

합니다 **/USEPROFILE** 링커 옵션은 Visual Studio 2015의 새로운 기능입니다.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 링커 옵션을 설정하려면

1. 프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 참조 하세요 [Visual c + + 프로젝트 속성 설정](../../ide/working-with-project-properties.md)합니다.

1. 선택 된 **구성 속성** > **링커** > **최적화** 속성 페이지.

1. 에 **링크 타임 코드 생성** 속성인 선택 **사용 하 여 링크 타임 코드 생성 (/ LTCG)** 합니다.

1. 선택 된 **구성 속성** > **링커** > **명령줄** 속성 페이지.

1. 입력 된 **/USEPROFILE** 옵션 및 선택적 인수에는 **추가 옵션** 상자. 선택할 **확인** 변경 내용을 저장 합니다.

### <a name="to-set-this-linker-option-programmatically"></a>프로그래밍 방식으로 이 링커 옵션을 설정하려면

- <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.AdditionalOptions%2A>을 참조하세요.

## <a name="see-also"></a>참고자료

[/GENPROFILE 및 /fastgenprofile은](genprofile-fastgenprofile-generate-profiling-instrumented-build.md)<br/>
[/LTCG](ltcg-link-time-code-generation.md)<br/>
[프로필 기반 최적화](../../build/reference/profile-guided-optimizations.md)<br/>
[프로필 기반 최적화 환경 변수](../../build/reference/environment-variables-for-profile-guided-optimizations.md)<br/>
