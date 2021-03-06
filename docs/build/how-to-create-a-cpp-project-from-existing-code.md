---
title: '방법: 기존 코드에서 C++ 프로젝트 만들기'
ms.date: 01/15/2019
helpviewer_keywords:
- C++, creating projects from existing code
- Create New Project From Existing Code Files Wizard, project settings
f1_keywords:
- vc.appwiz.importwiz.location
- vc.appwiz.importwiz.appsettings
- vc.appwiz.importwiz.debugsettings
- vc.appwiz.importwiz.releasesettings
ms.assetid: e328a938-395c-48ea-9e35-dd433de12b31
ms.openlocfilehash: 1658e19595d8cfc7966ca881abfdd2aa8acf76ab
ms.sourcegitcommit: 8105b7003b89b73b4359644ff4281e1595352dda
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57827352"
---
# <a name="how-to-create-a-c-project-from-existing-code"></a>방법: 기존 코드에서 C++ 프로젝트 만들기

Visual Studio에서 **기존 코드 파일에서 새 프로젝트 만들기** 마법사를 사용하여 기존 코드 파일을 C++ 프로젝트로 이식할 수 있습니다. 이 마법사는 MSBuild 시스템을 사용하여 원본 파일을 관리하고 구성을 빌드하는 프로젝트 솔루션을 만듭니다. 복잡한 폴더 계층이 없는 비교적 간단한 프로젝트일 때 가장 잘 작동합니다. 이 마법사는 Visual Studio의 이전 Express 버전에서는 사용할 수 없습니다. 

기존 코드 파일을 C++ 프로젝트로 이식하면 IDE에 기본 제공되는 기본 MSBuild 프로젝트 관리 기능을 사용할 수 있습니다. nmake 메이크파일, CMake 또는 대체 파일 같은 기존 빌드 시스템을 선호하는 경우 CMake 옵션 대신 폴더 열기를 사용하면 됩니다. 자세한 내용은 [c + +의 폴더 열기 프로젝트](open-folder-projects-cpp.md) 하거나 [Visual Studio의 CMake 프로젝트](cmake-projects-in-visual-studio.md)합니다. 두 옵션을 모두 사용하면 [IntelliSense](/visualstudio/ide/using-intellisense) 및 [프로젝트 속성](working-with-project-properties.md)과 같은 IDE 기능을 사용할 수 있습니다.

### <a name="to-create-a-c-project-from-existing-code"></a>기존 코드에서 C++ 프로젝트를 만들려면

1. **파일** 메뉴에서 **새로 만들기** > **기존 코드의 프로젝트**를 선택합니다.

1. **기존 코드 파일에서 새 프로젝트 만들기** 마법사의 첫 페이지에 있는 **만들 프로젝트 형식** 목록에서 **Visual C++** 를 선택합니다. **다음** 을 선택하여 계속 진행합니다.

1. 프로젝트 위치, 원본 파일의 디렉터리, 마법사가 새 프로젝트로 가져오는 파일 종류를 지정합니다. **다음** 을 선택하여 계속 진행합니다.

    | 설정 | 설명 |
    | --- | --- |
    | **프로젝트 파일 위치** | 새 프로젝트의 디렉터리 경로를 지정합니다. 이 위치에 마법사가 새 프로젝트의 모든 파일(및 하위 디렉터리)을 저장합니다.<br/><br/>**찾아보기**를 선택하여 **프로젝트 파일 위치** 대화 상자를 표시합니다. 해당 폴더로 이동하여 새 프로젝트가 포함된 디렉터리를 지정합니다. |
    | **프로젝트 이름** | 새 프로젝트의 이름을 지정합니다. .vcxproj 같은 파일 확장명을 갖는 프로젝트 파일은 이 이름을 채택하고 기존 코드 파일은 원래 이름을 유지합니다. |
    | **이 폴더의 파일을 프로젝트에 추가** | 원래 디렉터리(이 컨트롤 아래 목록 상자에 지정됨)의 기존 코드 파일을 새 프로젝트로 복사하도록 마법사를 설정하려면 이 옵션을 선택합니다.<br/><br/>모든 하위 디렉터리의 코드 파일을 프로젝트로 복사하도록 지정하려면 **하위 폴더 추가**를 선택합니다. 디렉터리는 **폴더** 열에 나열됩니다.<br/>- **이 폴더에서 프로젝트에 파일 추가** 대화 상자를 표시하고 마법사가 기존 코드 파일을 검색하는 디렉터리를 지정하려면 **추가**를 선택합니다.<br/>- 목록 상자에서 선택한 디렉터리 경로를 삭제하려면 **제거**를 선택합니다.<br/><br/>**프로젝트에 추가할 파일 형식** 상자에서, 마법사가 지정된 파일 확장명에 따라 새 프로젝트에 추가할 파일 종류를 지정합니다. 파일 확장명 앞에는 별표 와일드카드 문자가 오며, 파일 확장명 목록은 세미콜론으로 구분됩니다. |
    | **솔루션 탐색기에 모든 파일 표시** | 새 프로젝트의 모든 파일을 **솔루션 탐색기** 창에 표시하도록 지정합니다. 기본적으로 이 옵션은 사용하도록 설정됩니다. |

    ![프로젝트 위치](media/location.png)

1. 사용할 프로젝트 설정(예: 새 프로젝트의 빌드 환경) 및 생성할 새 프로젝트의 형식에 맞는 빌드 설정을 지정합니다. **다음** 을 선택하여 계속 진행합니다.

    | 설정 | 설명 |
    | --- | --- |
    | **Visual Studio 사용** | 새 프로젝트를 빌드할 때 Visual Studio에 포함된 빌드 도구를 사용하도록 지정합니다. 이 옵션은 기본적으로 선택됩니다.<br/><br/>**프로젝트 형식**을 선택하여 마법사에서 생성하는 프로젝트 형식을 지정합니다. **Windows 애플리케이션 프로젝트**, **콘솔 애플리케이션 프로젝트**, **DLL(동적 연결 라이브러리) 프로젝트** 또는 **LIB(정적 라이브러리) 프로젝트**를 선택합니다.<br/><br/>새 프로젝트에 ATL 지원을 추가하려면 **ATL에 대한 지원 추가**를 선택합니다.<br/><br/>새 프로젝트에 MFC 지원을 추가하려면 **MFC에 대한 지원 추가**를 선택합니다.<br/><br/>프로젝트에 CLR 프로그래밍 지원을 추가하려면 **공용 언어 런타임에 대한 지원 추가**를 선택합니다. 규정 준수 형식에 대한 **공용 언어 런타임 지원**을 선택합니다. 예를 들어 Visual C++ 2005 이전의 CLR 프로그래밍 구문인 Managed Extensions for C++ 구문을 준수하도록 **공용 언어 런타임(이전 구문)** 을 선택합니다. |
    | **외부 빌드 시스템 사용** | 새 프로젝트를 빌드할 때 Visual Studio에 포함되지 않는 빌드 도구를 사용하도록 지정합니다. 이 옵션을 선택하면 **디버그 구성 설정 지정** 및 **릴리스 구성 설정 지정** 페이지에서 빌드 명령줄을 지정할 수 있습니다. |

    ![프로젝트 설정](media/settings.png)

    > [!NOTE]
    > **외부 빌드 시스템 사용** 옵션을 선택하면 IDE가 프로젝트를 빌드하지 않으므로 컴파일에 /D, /I, /FI, /AI 또는 /FU 옵션이 필요 없습니다. 그러나 IntelliSense가 제대로 작동하려면 이러한 옵션을 순서대로 올바르게 설정해야 합니다.

1. 사용할 디버그 구성 설정을 지정합니다. **다음** 을 선택하여 계속 진행합니다.

    | 설정 | 설명 |
    | --- | --- |
    | **빌드 명령줄** | 프로젝트를 빌드하는 명령줄을 지정합니다. 프로젝트를 빌드하는 데 사용할 컴파일러(및 모든 스위치 또는 인수) 또는 빌드 스크립트의 이름을 입력합니다. |
    | **다시 빌드 명령줄** | 새 프로젝트를 다시 빌드하는 명령줄을 지정합니다. |
    | **정리 명령줄** | 프로젝트에 대한 빌드 도구에서 생성한 지원 파일을 삭제하도록 명령줄을 지정합니다. |
    | **출력(디버깅용)** | 프로젝트의 디버그 구성에 대한 출력 파일의 디렉터리 경로를 지정합니다. |
    | **전처리기 정의(/D)** | 프로젝트에 대한 전처리기 기호를 정의합니다. [/D(전처리기 정의)](../build/reference/d-preprocessor-definitions.md)를 참조하세요. |
    | **포함 검색 경로(/I)** | 컴파일러가 프로젝트에서 전처리기 지시문에 전달된 파일 참조를 확인하기 위해 검색할 디렉터리 경로를 지정합니다. [/I(추가 포함 디렉터리)](../build/reference/i-additional-include-directories.md)를 참조하세요. |
    | **강제 포함 파일(/FI)** | 프로젝트를 빌드할 때 처리할 헤더 파일을 지정합니다. [/FI(강제 포함 파일 이름 지정)](../build/reference/fi-name-forced-include-file.md)를 참조하세요. |
    | **.NET 어셈블리 검색 경로(/AI)** | 컴파일러가 프로젝트에서 전처리기 지시문에 전달된 .NET 어셈블리 참조를 확인하기 위해 검색할 디렉터리 경로를 지정합니다. [/AI(메타데이터 디렉터리 지정)](../build/reference/ai-specify-metadata-directories.md)를 참조하세요. |
    | **강제 사용 .NET 어셈블리(/FU)** | 프로젝트를 빌드할 때 처리할 .NET 어셈블리를 지정합니다. [/FU(강제 #using 파일 이름 지정)](../build/reference/fu-name-forced-hash-using-file.md)를 참조하세요. |

    ![프로젝트 구성](media/config.png)

    > [!NOTE]
    > **빌드**, **다시 필드**, **정리** 명령줄 및 **출력(디버깅용)** 설정은 **프로젝트 설정 지정** 페이지에서 **외부 빌드 시스템 사용** 옵션을 선택한 경우에만 사용됩니다.

1. 사용할 릴리스 구성 설정을 지정하세요. 이러한 설정은 디버그 구성 설정과 동일합니다. **마침**을 선택하여 새 프로젝트를 생성합니다.

    > [!NOTE]
    > 마법사가 디버그 구성 프로젝트 설정과 동일한 릴리스 구성 프로젝트 설정을 생성하도록 지정하려면 여기서 **디버그 구성과 동일**을 선택합니다. 기본적으로 이 옵션은 선택되어 있습니다. 이 상자의 선택을 취소하지 않으면 이 페이지의 다른 모든 옵션이 비활성화됩니다.
