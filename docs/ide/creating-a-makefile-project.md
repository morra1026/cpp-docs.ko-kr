---
title: C++ 메이크파일 프로젝트 만들기
ms.date: 10/19/2018
f1_keywords:
- vc.appwiz.makefile.project
helpviewer_keywords:
- Makefile projects, creating
- project files [C++], Makefile projects
ms.assetid: dd077af3-97a8-48fb-baaa-cf7e07ddef61
ms.openlocfilehash: 0c64f6df342e82e3ea5409e2b07af1e591747d7c
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50494850"
---
# <a name="creating-a-c-makefile-project"></a>C++ 메이크파일 프로젝트 만들기

‘메이크파일’은 C++ 소스 코드 파일 집합을 컴파일하고 링크(또는 ‘빌드’)하는 방법에 대한 지시를 포함하는 텍스트 파일입니다. ‘메이크’ 프로그램은 메이크파일을 읽고, 컴파일러, 링커 및 가능한 다른 프로그램을 호출하여 실행 파일을 만듭니다. ‘메이크’ 프로그램의 Microsoft 구현을 **NMAKE**라고 합니다. (Visual Studio는 기본적으로 .vcxproj 파일을 기반으로 하는 MSBuild 시스템을 사용합니다. 이 파일은 **파일 | 새로 만들기 | 프로젝트**에서 만드는 항목입니다.)

기존 메이크파일 프로젝트가 있는 경우 Visual Studio IDE에서 코딩 및/또는 디버그할지 선택 사항이 있습니다.

- Visual Studio에서 기존 메이크파일을 사용하여 IDE에서 코드를 빌드하는 메이크파일 프로젝트를 만듭니다. (기본 MSBuild 프로젝트를 사용하여 다운로드하는 IDE 기능이 일부 없습니다.) 아래의 [메이크파일 프로젝트 만들기](#create_a_makefile_project)를 참조하세요.
- **기존 코드 파일에서 새 프로젝트 만들기** 마법사를 사용하여 소스 코드에서 기본 MSBuild 프로젝트를 만듭니다. 자세한 내용은 [방법: 기존 코드로 C++ 프로젝트 만들기](how-to-create-a-cpp-project-from-existing-code.md)를 참조하세요.
- **Visual Studio 2017 이상**: **폴더 열기** 기능을 사용하여 MSBuild로 변환하지 않고 메이크파일 프로젝트를 엽니다. 자세한 내용은 [Visual C++의 폴더 열기 프로젝트](non-msbuild-projects.md)를 참조하세요.

## <a name="a-namecreateamakefileproject-to-create-a-makefile-project-with-the-makefile-project-template"></a><a name="create_a_makefile_project"> 메이크파일 프로젝트 템플릿을 사용하여 메이크파일 프로젝트 만들기

Visual Studio 2017 이상에서 메이크파일 프로젝트 템플릿은 C++ 데스크톱 개발 워크로드가 설치되어 있을 때 사용할 수 있습니다.

마법사를 따라 메이크파일에서 사용하는 명령과 환경을 지정합니다. 그러면 이 프로젝트를 사용하여 Visual Studio 개발 환경에서 코드를 빌드할 수 있습니다.

기본적으로 메이크파일 프로젝트는 솔루션 탐색기에 파일을 표시하지 않습니다. 메이크파일 프로젝트는 프로젝트의 속성 페이지에 반영되는 빌드 설정을 지정합니다.

프로젝트에서 지정하는 출력 파일은 빌드 스크립트가 생성하는 이름에는 영향을 미치지 않으며 의도만 선언합니다. 메이크파일은 여전히 빌드 프로세스를 제어하고 빌드 대상을 지정합니다.

1. Visual Studio 시작 페이지에서 **새 프로젝트** 검색 상자에 “메이크파일”을 입력합니다. 또는 **새 프로젝트** 대화 상자에서 **Visual C++** > **일반**(Visual Studio 2015) 또는 **기타**(Visual Studio 2017)를 확장한 다음, [템플릿] 창에서 **메이크파일 프로젝트**를 선택하여 프로젝트 마법사를 엽니다.

1. [응용 프로그램 설정](../ide/application-settings-makefile-project-wizard.md) 페이지에서 디버그 및 일반 정품 빌드에 대한 명령, 출력, 정리 및 다시 빌드 정보를 제공합니다.

1. **마침**을 클릭하여 마법사를 닫고, **솔루션 탐색기**에서 새로 만든 프로젝트를 엽니다.

속성 페이지에서 프로젝트의 속성을 보고 편집할 수 있습니다. 속성 페이지를 표시하는 방법에 대한 자세한 내용은 [Visual C++ 프로젝트 속성 설정](../ide/working-with-project-properties.md)을 참조하세요.

## <a name="see-also"></a>참고 항목

[메이크파일 프로젝트 마법사](../ide/makefile-project-wizard.md)<br/>
[메이크파일의 특수 문자](../build/special-characters-in-a-makefile.md)<br/>
[메이크파일의 내용](../build/contents-of-a-makefile.md)<br/>
