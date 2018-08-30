---
title: -실행-문자 집합 (실행 문자 집합 설정) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp
- devlang-cpp
ms.topic: reference
f1_keywords:
- execution-charset
- /execution-charset
dev_langs:
- C++
helpviewer_keywords:
- /execution-charset compiler option
- -execution-charset compiler option
ms.assetid: 0e02f487-2236-45bc-95f3-5760933a8f96
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 02f3e4273e9fc4064b26c6e32d708c4e6d586ae1
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43212674"
---
# <a name="execution-charset-set-execution-character-set"></a>/execution-charset (실행 문자 집합 설정)
실행 문자 집합에 실행 파일을 지정할 수 있습니다.  
  
## <a name="syntax"></a>구문  
  
```  
/execution-charset:[IANA_name|.CPID]  
```  
  
## <a name="arguments"></a>인수  
 **IANA_name**  
 IANA 정의한 문자 집합 이름입니다.  
  
 **CPID**  
 코드 페이지 식별자입니다.  
  
## <a name="remarks"></a>설명  
 사용할 수는 **/execution-charset** 실행 문자 집합을 지정 하는 옵션입니다. 실행 문자 집합에는 모든 단계를 전처리 하는 컴파일 단계를 입력 하는 프로그램의 텍스트에 사용 되는 인코딩입니다. 이 문자 집합은 컴파일된 코드에서 문자열 또는 문자 리터럴을 내부 표현에 사용 됩니다. 기본 실행 문자 집합으로 표현할 수 없는 문자를 포함 하는 소스 파일을 사용 하는 확장 된 실행 문자 집합을 지정 하려면이 옵션을 설정 합니다. IANA 중 하나를 사용할 수 있습니다 또는 ISO 문자 집합 이름을 사용 하도록 설정 하는 문자를 지정 하려면 3 ~ 5 자리 10 진수 코드 페이지 식별자가 뒤에 점 (.). 문자 집합 이름 목록이 지원 코드 페이지 식별자를 참조 하세요 [코드 페이지 식별자](/windows/desktop/Intl/code-page-identifiers)합니다.  
  
 Visual Studio는 기본적으로 인지 하는 경우 소스 파일 인코딩된 유니코드 형식으로 예를 들어, utf-16 또는 u t F-8 바이트 순서 표시를 검색 합니다. 바이트 순서 표시가 없는 경우 소스 파일은 인코딩된 현재 사용자 코드 페이지를 사용 하 여 지정한 문자를 사용 하 여 이름 또는 코드 페이지를 설정 하지 않는 한 가정 합니다 **/source-charset** 옵션 또는 **/utf-8** 옵션입니다. Visual Studio를 사용 하면 여러 문자 인코딩 중 하나를 사용 하 여 c + + 소스 코드를 저장할 수 있습니다. 소스 및 실행 문자 집합에 대 한 정보를 참조 하세요 [문자 집합](../../cpp/character-sets.md) 언어 설명서에 있습니다.  
  
 소스 문자 집합과 실행 문자 집합 모두 u t F-8로 설정 하려는 경우 사용할 수 있습니다 합니다 **/utf-8** 바로 가기로 컴파일러 옵션입니다. 지정 하는 것과 같습니다 **원본-charset:utf-8 /execution-charset:utf-8** 명령줄에서. 이러한 옵션도 사용 하도록 설정 합니다 **/validate-charset** 옵션이 기본적으로 합니다.  
  
### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Visual Studio 개발 환경에서 이 컴파일러 옵션을 설정하려면  
  
1.  프로젝트 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)을 참조하세요.  
  
2.  확장 된 **구성 속성**, **C/c + +** 를 **명령줄** 폴더입니다.  
  
3.  **고급 옵션**를 추가 합니다 **/execution-charset** 옵션을 선택한 기본 인코딩을 지정 합니다.  
  
4.  선택할 **확인** 변경 내용을 저장 합니다.  
  
## <a name="see-also"></a>참고 항목  
 [컴파일러 옵션](../../build/reference/compiler-options.md)   
 [컴파일러 옵션 설정](../../build/reference/setting-compiler-options.md)   
 [/source-charset (소스 문자 집합 설정)](../../build/reference/source-charset-set-source-character-set.md)   
 [/utf-8 (소스 및 실행 문자 집합을 u t F-8)](../../build/reference/utf-8-set-source-and-executable-character-sets-to-utf-8.md)   
 [/validate-charset(호환 문자에 대한 유효성 검사)](../../build/reference/validate-charset-validate-for-compatible-characters.md)