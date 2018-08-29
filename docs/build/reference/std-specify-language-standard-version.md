---
title: -std (언어 표준 버전 지정) | Microsoft Docs
ms.custom: ''
ms.date: 11/16/2017
ms.topic: reference
f1_keywords:
- /std
- -std
- VC.Project.VCCLCompilerTool.CppLanguageStandard
dev_langs:
- C++
ms.assetid: 0acb74ba-1aa8-4c05-b96c-682988dc19bd
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 2b3254d61295e0cfe0fc398e4aa2a2f2a926dbb1
ms.sourcegitcommit: f7703076b850c717c33d72fb0755fbb2215c5ddc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/28/2018
ms.locfileid: "43130912"
---
# <a name="std-specify-language-standard-version"></a>/std (언어 표준 버전 지정)

사용에서 지정된 된 버전의 c + + 언어 표준 c + + 언어 기능을 지원 합니다.

## <a name="syntax"></a>구문

> /std: [c + + 14 | c + + 17 | 최신 c + +]

## <a name="remarks"></a>설명

합니다 **/std** 옵션은 이상 Visual Studio 2017에서 사용할 수 있습니다. 버전별 ISO c + + 프로그래밍 코드를 컴파일할 때 사용 하도록 설정 하는 언어 표준 기능을 제어 하는 것이 됩니다. 이 옵션을 사용 하면 표준 언어의 특정 버전을 준수 하는 기존 코드를 손상 시킬 수 있는 일부 새로운 언어 및 라이브러리 기능에 대 한 지원을 사용 하지 않도록 설정할 수 있습니다. 기본적으로 **/std: c + + 14** 지정 된 언어 및 표준 c + + 언어의 이후 버전에서 발견 된 표준 라이브러리 기능이 사용 하지 않도록 설정 하는 합니다. 사용 하 여 **/std: c + + 17** c++17 표준 관련 기능 및 동작을 사용 하도록 설정 합니다. 지원 되는 최신 컴파일러 및 표준 라이브러리 기능을 명시적으로 사용 하려면 **/std: c + + 최신**합니다.

기본값 **/std: c + + 14** 옵션을 사용 하면 C + + 14 기능 집합 Visual c + + 컴파일러에서 구현 합니다. 이 옵션은 컴파일러 및 일부 c++17 기능 이미 구현 되어 이전 버전의 Visual c + + 컴파일러를 제외 하 고 표준 언어의 최신 버전의 새로운 변경 된 기능에 대 한 또는 표준 라이브러리 지원을 사용 하지 않도록 설정 합니다. Visual Studio 2015 업데이트 2부터 제공 되는 기능에서 종속성을 이미 사용 하는 사용자에 대해 상당한 변화를 방지 하려면이 기능이 계속 사용 되도록 설정 될 때를 **/std: c + + 14** 옵션을 지정 합니다.

- [중괄호로 묶인 init 목록을 사용한 auto에 대 한 규칙](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n3922.html)

- [템플릿 template-parameters의 typename](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4051.html)

- [삼중 자 제거](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4086.html)

- [네임 스페이스 및 열거자에 대 한 특성](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4266.html)

- [u8 문자 리터럴](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4267.html)

추가 정보에 대 한 기능에 따라 C + + 14 및 C + + 17 설정 된 경우 **/std: c + + 14** 는 지정에서 정보를 참조 하십시오 [Visual c + + 언어 규칙](../../visual-cpp-language-conformance.md)합니다.
  
합니다 **/std: c + + 17** 옵션을 사용 하면 전체 C + + 17 기능 집합 Visual c + + 컴파일러에서 구현 합니다. 이 옵션에서는 C++17 이후의 C++표준 규격 초안(Working Draft) 및 결함 업데이트의 전에서 변경되거나 새로운 기능에 대한 컴파일러 및 표준 라이브러리 지원을 사용하지 않습니다.  
  
합니다 **/std: c + + 최신** 가장 추적 하려면 Visual c + +에서 구현 된 c + + 언어 및 라이브러리 기능 집합 옵션을 사용 하면 최신 C + + 20 초안 작업 및 결함 업데이트의 c + + 표준 C + + 17에 포함 되지 않은 합니다. 이 스위치를 사용 하 여 가져오기는 게시-컴파일러 및 표준 라이브러리를 지 원하는 C + + 17 개의 언어 기능입니다. 지원 되는 언어 및 라이브러리 기능 목록을 참조 하세요 [Visual c + +에 대 한 새로운](../../what-s-new-for-visual-cpp-in-visual-studio.md)합니다. 합니다 **/std: c + + 최신** 옵션에 의해 보호 기능 사용 되지 않습니다는 **실험적 /** 전환 합니다.  
  
합니다 **/std** c + + 컴파일하는 동안 적용 옵션을 사용 하 여 검색할 수는 [ \_MSVC\_LANG](../../preprocessor/predefined-macros.md) 전처리기 매크로입니다. 자세한 내용은 [전처리기 매크로](../../preprocessor/predefined-macros.md)합니다.

합니다 **/std: c + + 14** 하 고 **/std: c + + 최신** 옵션은 Visual c + + 2015 업데이트 3부터 사용할 수 있습니다. 합니다 **/std: c + + 17** 옵션은 Visual c + + 2017 버전 15.3부터 사용할 수 있습니다. 동작으로 활성화 되어 일부 c++17 표준 위에서 설명한 것 처럼 합니다 **/std: c + + 14** 옵션을 사용 하지만 다른 모든 C + + 17 기능으로 사용 됩니다 **/std: c + + 17**합니다.
  
> [!NOTE]
> Visual c + + 컴파일러 버전 또는 업데이트 수준에 따라 특정 C + + 14 또는 C + + 17 기능 하지 구현 될 수 있습니다 완전히 또는 완전히와 호환 되는 지정 하는 경우는 **/std: c + + 14** 또는 **/std: c + + 17** 옵션입니다. 예를 들어, Visual c + + 2017 RTM 컴파일러가 C + + 14을 준수 하는 완벽 하 게 지원 하지 않습니다 `constexpr`, SFINAE 식 또는 2 단계 이름 조회 합니다. 릴리스 버전에서 Visual c + +에서 c + + 언어 규칙의 개요를 보려면 [Visual c + + 언어 규칙](../../visual-cpp-language-conformance.md)합니다. 
  
### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 컴파일러 옵션을 설정하려면  
  
1.  프로젝트의 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.  
  
2.  선택 **구성 속성**를 **C/c + +** 하십시오 **언어**합니다.  
  
3.  **c + + 언어 표준을**를 선택 하기 위해 선택한 드롭다운 컨트롤에서 지 원하는 언어 표준을 **확인** 또는 **적용** 변경 내용을 저장 하려면.  
  
## <a name="see-also"></a>참고자료  
  
[컴파일러 옵션](../../build/reference/compiler-options.md)   
[컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md)   
