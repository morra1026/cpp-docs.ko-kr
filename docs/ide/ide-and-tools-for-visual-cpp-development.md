---
title: IDE 및 Visual C++ 개발 도구 | Microsoft Docs
description: Visual Studio IDE는 코드 편집기, 디버거, 테스트 프레임워크, 정적 분석기 및 기타 프로그래밍 도구를 사용하여 Windows, Linux, Android 및 iOS에서 C++ 개발을 수행하도록 지원합니다.
ms.custom: ''
ms.date: 09/27/2018
ms.technology:
- cpp-ide
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- Visual C++, development tools
ms.assetid: 56eabafb-1956-4f0f-bec5-29b887763559
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 310dc9b8e31f72fbd04c620987d9857932f7a0a1
ms.sourcegitcommit: a738519aa491a493a8f213971354356c0e6a5f3a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/05/2018
ms.locfileid: "48821151"
---
# <a name="ide-and-compiler-tools-for-visual-c-development"></a>IDE 및 Visual C++ 개발을 위한 컴파일러 도구

Visual Studio IDE(통합 개발 환경)의 일부인 Microsoft Visual C++(MSVC)는 다른 언어와 공통된 다양한 창과 도구를 공유합니다. **솔루션 탐색기**, 코드 편집기 및 디버거를 비롯한 이러한 창과 도구에 대해서는 [Visual Studio IDE](/visualstudio/ide/visual-studio-ide)에서 설명합니다. 공유 도구 또는 창에 있는 C++용 기능 집합과 .NET 언어 또는 JavaScript용 기능 집합이 약간 다른 경우가 자주 있습니다. 일부 창이나 도구는 Visual Studio Professional 또는 Visual Studio Enterprise 버전에서만 사용할 수 있습니다.

Visual Studio IDE에 있는 공유 도구 외에도, MSVC에는 네이티브 코드 개발 전용으로 사용되는 여러 도구가 있습니다. 이러한 도구의 목록도 이 문서에서 제공합니다. Visual Studio의 각 버전에서 사용할 수 있는 도구 목록은 [Visual Studio 버전의 Visual C++ 도구 및 기능](visual-cpp-tools-and-features-in-visual-studio-editions.md)을 참조하세요.

## <a name="create-projects"></a>프로젝트 만들기

*프로젝트*는 기본적으로 실행 파일에 빌드된 이미지 또는 데이터 파일과 같은 소스 코드 파일 및 리소스 집합입니다. 

Visual Studio 2015는 MSBuild 프로젝트에 대한 지원을 제공합니다. Qt 또는 CMake와 같은 다른 빌드 시스템에 대한 Visual Studio 확장을 다운로드할 수 있습니다.

Visual Studio 2017은 IntelliSense, 검색 및 디버깅을 완벽하게 지원하여 사용자가 사용하기를 원하는 모든 빌드 시스템 또는 사용자 지정 빌드 도구에 대한 지원을 제공합니다.

- **MSBuild**는 Visual Studio용 네이티브 빌드 시스템입니다. 주 메뉴에서 **파일** > **새로 만들기** > **프로젝트**를 선택하면 다양한 종류의 C++ 응용 프로그램 개발을 빠르게 시작하기 위한 많은 유형의 MSBuild ‘프로젝트 템플릿’이 표시됩니다.

   ![프로젝트 템플릿](media/vs2017-new-project.png " Visual Studio 2017 새 프로젝트 대화 상자")

   일반적으로, CMake 또는 다른 프로젝트 시스템을 사용해야 하는 구체적인 이유가 없으면 새 프로젝트에서 이러한 템플릿을 사용하는 것이 좋습니다. 일부 프로젝트에는 새 프로젝트를 만드는 과정을 단계별로 안내하는 *마법사*가 있습니다. 자세한 내용은 [MSBuild 기반 프로젝트 만들기 및 관리](creating-and-managing-visual-cpp-projects.md)를 참조하세요.

- **CMake**는 C++ 워크로드로 데스크톱 개발을 설치할 때, Visual Studio IDE에 통합되는 플랫폼 간 빌드 시스템입니다. 자세한 내용은 [Visual C++의 CMake 프로젝트](cmake-tools-for-visual-cpp.md)를 참조하세요.
- 느슨한 파일 컬렉션을 포함한 다른 모든 C++ 빌드 시스템은 **폴더 열기** 기능을 통해 지원됩니다. 간단한 JSON 파일을 생성하여 빌드 프로그램을 호출하고 디버깅 세션을 구성합니다. 자세한 내용은 [Visual C++의 폴더 열기 프로젝트](non-msbuild-projects.md)를 참조하세요.

## <a name="add-to-source-control"></a>소스 제어에 추가

소스 제어를 사용하면 여러 개발자 간 작업을 조정하고, 진행 중인 작업을 프로덕션 코드에서 분리하고, 소스 코드를 백업할 수 있습니다. Visual Studio에서는 해당 **팀 탐색기** 창을 통해 Git 및 [TFVC\(Team Foundation 버전 제어\)](/azure/devops/repos/tfvc/)를 지원합니다.

![팀 탐색기](media/vs2017-team-explorer.png "Visual Studio 2017 팀 탐색기")

Azure의 리포지토리와의 Git 통합에 대한 자세한 내용은 [Visual Studio 2017 및 Azure 리포지토리 Git과 코드 공유](/azure/devops/repos/git/share-your-code-in-git-vs-2017)를 참조하세요. GitHub와의 Git 통합에 대한 자세한 내용은 [Visual Studio용 GitHub 확장](https://visualstudio.github.com/)을 참조하세요.

## <a name="create-user-interfaces-with-designers"></a>디자이너를 사용하여 사용자 인터페이스 만들기

프로그램에 사용자 인터페이스가 있는 경우 디자이너를 사용하여 단추, 목록 상자 등의 컨트롤로 빠르게 채울 수 있습니다. 도구 상자 창의 컨트롤을 끌어 디자인 화면에 놓으면 Visual Studio에서 모든 작업을 수행하는 데 필요한 리소스 및 코드를 생성합니다. 그런 다음, 코드를 작성하여 모양 및 동작을 사용자 지정합니다.

![디자이너 및 도구 상자](media/vs2017-toolbox-designer.png "Visual Studio 2017 도구 상자 및 디자이너")

유니버설 Windows 플랫폼 앱의 사용자 인터페이스 디자인에 대한 자세한 내용은 [디자인 및 UI](https://developer.microsoft.com/en-us/windows/design)를 참조하세요.

MFC 응용 프로그램의 사용자 인터페이스 만드는 방법에 대한 자세한 내용은 [MFC 데스크톱 응용 프로그램](../mfc/mfc-desktop-applications.md)을 참조하세요. Win32 Windows 프로그램에 대한 자세한 내용은 [Windows 데스크톱 응용 프로그램](../windows/windows-desktop-applications-cpp.md)을 참조하세요.

## <a name="write-code"></a>코드 작성

프로젝트를 만든 후에는 모든 프로젝트 파일이 **솔루션 탐색기** 창에 표시됩니다. (*솔루션*은 하나 이상의 관련 프로젝트의 논리적 컨테이너입니다.) **솔루션 탐색기**에서 .h 또는 .cpp 파일을 클릭하면 파일이 코드 편집기에서 열립니다. 

![솔루션 탐색기 및 코드 편집기](media/vs2017-solution-explorer-code-editor.png "Visual Studio 2017 솔루션 탐색기 및 코드 편집기")

코드 편집기는 C++ 소스 코드용 특수 워드 프로세서입니다. 언어 키워드, 메서드 및 변수 이름, 기타 코드 요소 등을 색으로 구분하여 코드를 더 쉽게 읽고 이해할 수 있도록 해 줍니다.

자세한 내용은 [코드 작성 및 리팩터링](writing-and-refactoring-code-cpp.md)을 참조하세요.

## <a name="add-and-edit-resources"></a>리소스 추가 및 편집

‘리소스’라는 용어에는 대화 상자, 아이콘, 이미지, 지역화 가능한 문자열, 시작 화면, 데이터베이스 연결 문자열 또는 실행 파일에 포함하려는 임의 데이터가 포함됩니다.

네이티브 데스크톱 C++ 프로젝트에서 리소스 추가 및 편집에 대한 자세한 내용은 [리소스 파일 작업](../windows/working-with-resource-files.md)을 참조하세요.

## <a name="build-compile-and-link"></a>빌드(컴파일 및 연결)

메뉴 모음에서 **빌드** > **솔루션 빌드**를 선택하거나 Ctrl+Shift+B 키 조합을 입력하여 프로젝트를 컴파일하고 연결합니다. 빌드 오류 및 경고는 오류 목록에 보고됩니다(Ctrl+\\, E). **출력** 창(Alt+2)은 빌드 프로세스에 대한 정보를 표시합니다.

![출력 창 및 오류 목록](media/vs2017-output-error-list.png "Visual Studio 2017 출력 창 및 오류 목록") MSBuild 구성에 대한 자세한 내용은 [프로젝트 속성 작업](working-with-project-properties.md) 및 [Visual Studio에서 C++ 프로젝트 빌드](building-cpp-projects-in-visual-studio.md)를 참조하세요.

컴파일러(cl.exe) 및 다양한 빌드 관련 독립 실행형 도구(예: NMAKE 및 LIB)를 명령줄에서 바로 사용할 수도 있습니다. 자세한 내용은 [명령줄에서 C/C++ 코드 빌드](../build/building-on-the-command-line.md) 및 [C/C++ 빌드 참조](../build/reference/c-cpp-building-reference.md)를 참조하세요.

## <a name="debug"></a>디버그

**F5** 키를 눌러 디버깅을 시작할 수 있습니다. 설정한 모든 중단점에서 실행이 일시 중단됩니다. 한 번에 한 줄씩 코드를 단계별로 진행하고, 변수 또는 레지스터의 값을 확인하고, 일부 경우에는 코드 변경 후 다시 컴파일하지 않고 디버깅을 계속할 수도 있습니다. 다음 그림에서는 중단점에서 실행이 중지되는 디버깅 세션을 보여 줍니다. 데이터 구조 멤버의 값은 **조사식 창**에 표시됩니다.

![디버깅 세션](media/vs2017-debug-watch.png "Visual Studio 2017 디버깅 세션")

자세한 내용은 [Visual Studio의 디버깅](/visualstudio/debugger/debugging-in-visual-studio)을 참조하세요.

## <a name="test"></a>테스트

Visual Studio에는 네이티브 C++ 및 C++/CLI에 대한 단위 테스트 프레임워크가 들어 있습니다. Boost.Test, Google Test 및 CTest도 지원됩니다. **테스트 탐색기** 창에서 테스트를 실행합니다.

![테스트 탐색기](media/cpp-test-explorer-passed.png "Visual Studio 2017 테스트 탐색기")

자세한 내용은 [단위 테스트를 사용하여 코드 확인](/visualstudio/test/unit-test-your-code) 및 [Visual Studio에서 C/C++에 대한 단위 테스트 작성](/visualstudio/test/writing-unit-tests-for-c-cpp)을 참조하세요.

## <a name="analyze"></a>분석

Visual Studio에는 소스 코드에서 잠재적인 문제를 감지할 수 있는 정적 코드 분석 도구가 포함되어 있습니다. 이러한 도구에는 [C++ Core Guidelines](https://github.com/isocpp/CppCoreGuidelines/blob/master/CppCoreGuidelines.md) 규칙 검사기의 구현이 포함됩니다. 자세한 내용은 [C/C++용 코드 분석 개요](/visualstudio/code-quality/code-analysis-for-c-cpp-overview)를 참조하세요.

## <a name="deploy-completed-applications"></a>완성된 응용 프로그램 배포

Microsoft Store를 통해 기존 데스크톱 응용 프로그램과 UWP 앱을 고객에게 배포할 수 있습니다. CRT 배포는 백그라운드에서 자동으로 처리됩니다. 자세한 내용은 [Windows 앱 및 게임 게시](/windows/uwp/publish/)를 참조하세요.

네이티브 C++ 데스크톱을 다른 컴퓨터에 배포할 수도 있습니다. 자세한 내용은 [데스크톱 응용 프로그램 배포](deploying-native-desktop-applications-visual-cpp.md)를 참조하세요.

C++/CLI 프로그램의 배포에 대한 자세한 내용은 [개발자를 위한 배포 가이드](/dotnet/framework/deployment/deployment-guide-for-developers)를 참조하세요.

## <a name="related-articles"></a>관련 문서

|||
|-|-|
|[Visual Studio 버전의 Visual C++ 도구 및 기능](visual-cpp-tools-and-features-in-visual-studio-editions.md)|다양한 Visual Studio 버전에서 사용할 수 있는 기능을 보여 줍니다.|
|[MSBuild 기반 프로젝트 만들기 및 관리](creating-and-managing-visual-cpp-projects.md)|Visual Studio의 C++ MSBuild 기반 프로젝트에 대한 개요와 해당 프로젝트를 만들고 관리하는 방법을 설명하는 다른 문서에 대한 링크를 제공합니다.|
|[Visual C++의 CMake 프로젝트](cmake-tools-for-visual-cpp.md).|Visual C++에서 CMake 또는 다른 비 MSBuild 프로젝트를 빌드하는 방법을 설명합니다.|
|[C/C++ 프로그램 빌드](../build/building-c-cpp-programs.md)|C++ 프로젝트를 빌드하는 방법을 설명합니다.|
|[데스크톱 응용 프로그램 배포](deploying-native-desktop-applications-visual-cpp.md)|C++ 앱 및 배포에 대해 자세히 설명하는 다른 문서로 연결되는 링크에 대한 개요를 제공합니다.|
|[Visual C++ 포팅 및 업그레이드 가이드](../porting/visual-cpp-porting-and-upgrading-guide.md)|이전 버전의 Visual Studio에서 만들어진 C++ 응용 프로그램을 업그레이드하는 방법 및 Visual Studio 이외의 다른 도구를 사용하여 생성된 응용 프로그램을 마이그레이션하는 방법에 대한 자세한 정보입니다.|
|[Visual C++](../visual-cpp-in-visual-studio.md)|Visual Studio에 포함된 Visual C++의 주요 기능을 설명하고 Visual C++ 설명서의 나머지 부분에 연결합니다.|
