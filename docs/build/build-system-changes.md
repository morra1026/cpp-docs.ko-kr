---
title: 빌드 시스템 변경 내용 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
f1_keywords:
- vc.msbuild.changes
dev_langs:
- C++
helpviewer_keywords:
- Build system changes, project file (.vcxprog)
- Build system changes, custom build rules
- Build system changes, MSBuild
- MSBuild, build system changes
- Build system changes, .vsprops
- Build system changes, $(Inherit)
- Build system changes, $(NoInherit)
ms.assetid: e564d95f-a6cc-4d97-b57e-1a71daf66f4a
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: e29d664824a01c0e2a0c0e738368f8d025a239ee
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43202159"
---
# <a name="build-system-changes"></a>빌드 시스템 변경 사항
MSBuild 시스템은 Visual C++ 프로젝트를 빌드하는 데 사용됩니다. 하지만 Visual Studio 2008 및 이전 버전에서는 VCBuild 시스템이 사용되었습니다. 특정 파일 형식 및 VCBuild에 의존 하는 개념 중 하나 존재 하지 않거나 현재 시스템에서 다르게 표현 됩니다. 이 문서는 현재 빌드 시스템의 차이점을 설명 합니다.  
  
## <a name="vcproj-is-now-vcxproj"></a>.vcproj.vcxproj 되었습니다.  
 프로젝트 파일에는 더 이상.vcproj 파일 확장명을 사용합니다. Visual Studio는 자동으로 현재 시스템에서 사용 되는 형식으로 이전 버전의 Visual c + +에서 생성 된 프로젝트 파일을 변환 합니다. 수동으로 프로젝트를 업그레이드 하는 방법에 대 한 자세한 내용은 참조 하세요. [/Upgrade (devenv.exe)](/visualstudio/ide/reference/upgrade-devenv-exe)합니다.  
  
 현재 릴리스에서 프로젝트 파일의 파일 이름 확장명은.vcxproj입니다.  
  
## <a name="vsprops-is-now-props"></a>.vsprops.props 되었습니다.  
 이전 릴리스에서 *프로젝트 속성 시트* 은.vsprops 파일 이름 확장명을 가진 XML 기반 파일입니다. 프로젝트 속성 시트를 사용 하 여 컴파일러나 링커 등의 빌드 도구에 대 한 스위치를 지정 하 고 사용자 정의 매크로 만들 수 있습니다.  
  
 현재 릴리스에서 프로젝트 속성 시트의 파일 이름 확장명은.props입니다.  
  
## <a name="custom-build-rules-and-rules-files"></a>사용자 지정 빌드 규칙 및.rules 파일  
 이전 릴리스에서 *규칙 파일* 는.rules 파일 이름 확장명을 가진 XML 기반 파일입니다. 규칙 파일을 사용 하 여 사용자 지정 빌드 규칙을 정의 하 고 Visual c + + 프로젝트의 빌드 프로세스로 통합할 수 있습니다. 자세한 내용은 출력 파일 또는 하나 이상의 파일 이름 확장명을 사용 하 여 연결할 수 있습니다, 사용자 지정 빌드 규칙을 입력된 파일 하나를 만드는 도구에 전달할 수 있습니다.  
  
 이 릴리스에서 사용자 지정 빌드 규칙은 세 가지 파일 형식,.xml,.props, 및.rules 파일 대신.targets로 표시 됩니다. 패키지가 마이그레이션되면 이전 버전의 Visual c + +를 사용 하 여 만든.rules 파일로 현재 버전에 해당 하는.xml,.props 및.targets 파일 생성 되 고 원래.rules 파일과 함께 프로젝트에 저장 합니다.  
  
> [!IMPORTANT]
>  현재 릴리스에서 IDE는 새로운 규칙 생성을 지원 하지 않습니다. 따라서 이전 버전의 Visual C++를 사용해서 생성된 프로젝트의 규칙 파일을 사용하는 가장 쉬운 방법은 프로젝트를 현재 버전으로 마이그레이션하는 방법입니다.  
  
## <a name="inheritance-macros"></a>상속 매크로  
 이전 릴리스에서 **$ (inherit)** 매크로 프로젝트 빌드 시스템에서 구성 된 명령줄에서 상속 된 속성이 나타나는 순서를 지정 합니다. 합니다 **$ (noinherit)** 매크로 $ (inherit) 무시할의 중복 된 단어 시키고 상속할 수는 상속 될 하지 하는 모든 속성이 있습니다. 예를 들어, 기본적으로는 $ (inherit) 매크로 사용 하면 사용 하 여 지정 된 파일을 [/I (추가 포함 디렉터리)](../build/reference/i-additional-include-directories.md) 컴파일러 명령줄에 추가할 수 있습니다.  
  
 현재 릴리스에서 상속 하나 이상의 리터럴 값 및 속성 매크로의 연결 속성의 값을 지정 하 여 지원 됩니다. 합니다 **$ (inherit)** 하 고 **$ (noinherit)** 매크로 지원 되지 않습니다.  
  
 다음 예제에서는 세미콜론으로 구분 된 목록 속성 페이지에서 속성에 할당 됩니다. 연결 목록으로 구성 됩니다 합니다  *\<값 >* 리터럴 및의 값을 `MyProperty` 매크로 표기법을 사용 하 여 액세스할 수 있는 속성을 **$(**  <em>MyProperty</em>**)** 합니다.  
  
```  
Property=<value>;$(MyProperty)  
```  
  
## <a name="vcxprojuser-files"></a>. vcxproj.user 파일  
 사용자 파일 (. vcxproj.user) 예제, 디버깅 및 배포 설정에 대 한 사용자별 속성을 저장 합니다. Vcxproj.user 파일 특정 사용자에 대해 모든 프로젝트에 적용 됩니다.  
  
## <a name="vcxprojfilters-file"></a>. vcxproj.filters 파일  
 때 **솔루션 탐색기** 필터 파일을 프로젝트에 파일을 추가 하는 데 사용 됩니다 (. vcxproj.filters) 위치를 정의 합니다 **솔루션 탐색기** 트리 보기는 파일이 추가 되는 파일 이름 확장명에 따라 합니다.  
  
## <a name="vc-directories-settings"></a>VC + + 디렉터리 설정  
 Visual c + + 디렉터리 설정에 지정 된 된 [VC + + Directories Property Page](../ide/vcpp-directories-property-page.md)합니다. Visual Studio의 이전 릴리스에서 디렉터리 설정 사용자 단위를 적용 하 고 sysincl.dat 파일에 제외 된 디렉터리 목록을 지정 합니다.  
  
 실행 하는 경우에 VC + + 디렉터리 설정을 변경할 수 없습니다 [devenv /resetsettings](/visualstudio/ide/reference/resetsettings-devenv-exe) 명령줄에서. 도 변경할 수 없습니다 설정을 열면를 **도구** 메뉴에서 클릭 **설정 가져오기 및 내보내기**를 선택한 후는 **모든 설정 다시 설정** 옵션입니다.  
  
 Visual c + +의 이전 버전에서 만든.vssettings 파일의 VC + + 디렉터리 설정을 마이그레이션하십시오. 엽니다는 **도구** 메뉴에서 클릭 **설정 가져오기 및 내보내기**를 선택 **선택한 환경 설정 가져오기**, 마법사의 지시에 따릅니다. 처음으로 Visual Studio을 시작 하는 경우 또는 합니다 **기본 환경 설정 선택** 대화 상자에서 **이전 버전에서 적합 한 설정을 마이그레이션한 및 기본 설정 외에도 적용 아래 선택한**합니다.  
  
## <a name="see-also"></a>참고 항목  
 [MSBuild(Visual C++)](../build/msbuild-visual-cpp.md)