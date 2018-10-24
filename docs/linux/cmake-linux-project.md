---
title: Visual Studio에서 Linux CMake 프로젝트 구성 | Microsoft Docs
description: Visual Studio에서 Linux CMake 프로젝트를 구성하는 방법
ms.custom: ''
ms.date: 07/20/2018
ms.reviewer: ''
ms.suite: ''
ms.technology:
- cpp-linux
ms.tgt_pltfrm: Linux
ms.topic: conceptual
ms.assetid: f8707b32-f90d-494d-ae0b-1d44425fdc25
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
- linux
ms.openlocfilehash: 0e735ece878797ffdcf89fffefa33473107ad3d5
ms.sourcegitcommit: 7098d64443ffbd4a47f30bc41753007b570b47e8
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49120566"
---
# <a name="configure-a-linux-cmake-project"></a>Linux CMake 프로젝트 구성

**Visual Studio 2017 버전 15.4 이상**<br/>
Visual Studio에 대한 Linux C++ 워크로드를 설치하면 Linux용 CMake 지원이 기본적으로 선택됩니다. 이제 CMake를 Visual Studio 프로젝트로 변환할 필요 없이 CMake를 사용하는 기존 코드 베이스에서 작업할 수 있습니다. 코드 베이스가 플랫폼 간 기반인 경우 Visual Studio 내에서 Windows와 Linux를 모두 대상으로 할 수 있습니다.

이 항목에서는 Visual Studio의 CMake 지원에 대한 기본 지식이 있다고 가정합니다. 자세한 내용은 [Visual C++용 CMake 도구](../ide/cmake-tools-for-visual-cpp.md)를 참조하세요. CMake 자체에 대한 자세한 내용은 [CMake를 사용하여 소프트웨어 빌드, 테스트 및 패키지](https://cmake.org/)를 참조하세요.

> [!NOTE]  
> Visual Studio에서 CMake가 지원되려면 CMake 3.8에 도입된 서버 모드 지원이 필요합니다. Microsoft 제공 CMake 변형의 경우 [https://github.com/Microsoft/CMake/releases](https://github.com/Microsoft/CMake/releases)에서 미리 빌드된 최신 바이너리를 다운로드합니다. 

## <a name="open-a-folder"></a>폴더 열기

시작하려면 주 메뉴에서 **파일** > **열기** > **폴더**를 선택하거나 명령줄에서 `devenv.exe <foldername>`을 입력합니다. 열린 폴더에는 소스 코드와 함께 CMakeLists.txt 파일이 있어야 합니다.
다음 예제에서는 간단한 CMakeLists.txt 파일과 .cpp 파일을 보여 줍니다.

```cpp
// hello.cpp

#include <iostream>

int main(int argc, char* argv[])
{
    std::cout << "Hello from Linux CMake" << std::endl;
}
```

CMakeLists.txt:

```cmd
project (hello-cmake)
add_executable(hello-cmake hello.cpp)
```

## <a name="choose-a-linux-target"></a>Linux 대상 선택

폴더를 여는 즉시 Visual Studio에서 CMakeLists.txt 파일을 구문 분석하고 **x86-Debug**의 Windows 대상을 지정합니다. Linux를 대상으로 지정하려면 프로젝트 설정을 **Linux-Debug** 또는 **Linux-Release**로 변경합니다.

기본적으로 Visual Studio는 **도구** > **옵션** > **플랫폼 간** > **연결 관리자** 아래에 있는 목록에서 첫 번째 원격 시스템을 선택합니다. 원격 연결이 발견되지 않으면 만들라는 메시지가 표시됩니다.

Linux 대상을 지정하면 Linux 컴퓨터에 소스가 복사됩니다. 그런 다음 Linux 컴퓨터에서 CMake가 실행되어 프로젝트에 대한 CMake 캐시가 생성됩니다.

![Linux에서 CMake 캐시 생성](media/cmake-linux-1.png "Linux에서 CMake 캐시 생성")

**Visual Studio 2017 버전 15.7 이상:**<br/>
원격 헤더에 IntelliSense 지원을 제공하기 위해 Visual Studio는 로컬 Windows 컴퓨터의 디렉터리에 IntelliSense를 자동으로 복사합니다. 자세한 내용은 [원격 헤더를 위한 IntelliSense](configure-a-linux-project.md#remote_intellisense)를 참조하세요.

## <a name="debug-the-project"></a>프로젝트 디버그

원격 시스템에서 코드를 디버그하려면 중단점을 설정하고, 프로젝트 설정 옆의 도구 모음 메뉴에서 CMake 대상을 시작 항목으로 선택하고, 도구 모음에서 **&#x23f5; 시작**을 선택하거나 F5 키를 누릅니다.

프로그램의 명령줄 인수를 사용자 지정하려면 **솔루션 탐색기**에서 실행 파일을 마우스 오른쪽 단추로 클릭하고 **디버그 및 시작 설정**을 선택합니다. 그러면 프로그램에 대한 정보가 들어 있는 launch.vs.json 구성 파일이 열리거나 만들어집니다. 추가 인수를 지정하려면 `args` JSON 배열에 추가합니다. 자세한 내용은 [Visual C++의 폴더 열기 프로젝트](../ide/non-msbuild-projects.md)를 참조하세요.

## <a name="configure-cmake-settings-for-linux"></a>Linux용 CMake 설정 구성

기본 CMake 설정을 변경하려면 주 메뉴에서 **CMake | CMake 설정 변경 | CMakeLists.txt**를 선택하거나 **솔루션 탐색기**에서 CMakeSettings.txt를 마우스 오른쪽 단추로 클릭하고 **CMake 설정 변경**을 선택합니다. 그러면 Visual Studio에서 프로젝트 설정 메뉴 항목에 나열된 기본 구성으로 채워진 `CMakeSettings.json`이라는 폴더에 새 파일을 만듭니다. 다음 예제에서는 이전 코드 예제에 기반을 둔 Linux-Debug에 대한 기본 구성을 보여 줍니다.

```json
{
      "name": "Linux-Debug",
      "generator": "Unix Makefiles",
      "remoteMachineName": "${defaultRemoteMachineName}",
      "configurationType": "Debug",
      "remoteCMakeListsRoot": "/var/tmp/src/${workspaceHash}/${name}",
      "cmakeExecutable": "/usr/local/bin/cmake",
      "buildRoot": "${env.LOCALAPPDATA}\\CMakeBuilds\\${workspaceHash}\\build\\${name}",
      "installRoot": "${env.LOCALAPPDATA}\\CMakeBuilds\\${workspaceHash}\\install\\${name}",
      "remoteBuildRoot": "/var/tmp/build/${workspaceHash}/build/${name}",
      "remoteInstallRoot": "/var/tmp/build/${workspaceHash}/install/${name}",
      "remoteCopySources": true,
      "remoteCopySourcesOutputVerbosity": "Normal",
      "remoteCopySourcesConcurrentCopies": "10",
      "remoteCopySourcesMethod": "rsync",
      "remoteCopySourcesExclusionList": [".vs", ".git"],
      "rsyncCommandArgs" : "-t --delete --delete-excluded",
      "remoteCopyBuildOutput" : "false",
      "cmakeCommandArgs": "",
      "buildCommandArgs": "",
      "ctestCommandArgs": "",
      "inheritEnvironments": [ "linux-x64" ]
}
```

`name` 값은 원하는 값으로 설정할 수 있습니다. `remoteMachineName` 값은 원격 시스템이 여러 개 있을 경우 대상으로 지정할 항목을 지정합니다. 이 필드에는 올바른 시스템을 선택할 수 있도록 IntelliSense가 활성화됩니다. `remoteCMakeListsRoot` 필드는 원격 시스템에서 프로젝트 소스가 복사될 위치를 지정합니다. `remoteBuildRoot` 필드는 원격 시스템에서 빌드 출력이 생성될 위치입니다. 또한 해당 출력은 `buildRoot`로 지정된 위치에 로컬로 복사됩니다. `remoteInstallRoot` 및 `installRoot` 필드는 CMake 설치를 수행하는 경우 적용되는 것을 제외하고 `remoteBuildRoot` 및 `buildRoot`와 비슷합니다. `remoteCopySources` 항목은 로컬 소스가 원격 머신에 복사되는지 여부를 제어합니다. 많은 파일이 있고 이미 원본과 직접 동기화한 경우 이 항목을 false로 설정할 수 있습니다. `remoteCopyOutputVerbosity` 값은 오류를 진단해야 하는 경우 복사 단계의 자세한 정도를 제어합니다. `remoteCopySourcesConcurrentCopies` 항목은 복사를 수행하기 위해 생성된 프로세스 수를 제어합니다. `remoteCopySourcesMethod` 값은 rsync 또는 sftp 중 하나일 수 있습니다. `remoteCopySourcesExclusionList` 필드를 사용하면 원격 머신에 복사된 내용을 제어할 수 있습니다. `rsyncCommandArgs` 값을 통해 복사의 rsync 메서드를 제어할 수 있습니다. `remoteCopyBuildOutput` 필드는 원격 빌드 출력이 로컬 빌드 폴더에 복사되는지 여부를 제어합니다.

추가 제어를 위해 사용할 수 있는 일부 선택적 설정이 있습니다.

```json
{
      "remotePreBuildCommand": "",
      "remotePreGenerateCommand": "",
      "remotePostBuildCommand": "",
}
```

이러한 옵션을 사용하면 빌드하기 전후 및 CMake 생성하기 전에 원격 상자에서 명령을 실행할 수 있습니다. 원격 상자에서 유효한 명령일 수 있습니다. 출력은 Visual Studio로 다시 파이핑됩니다.

## <a name="download-prebuilt-cmake-binaries"></a>미리 빌드된 CMake 바이너리 다운로드

Linux distro에 이전 버전의 CMake가 있을 수 있습니다. Visual Studio에서 CMake가 지원되려면 CMake 3.8에 도입된 서버 모드 지원이 필요합니다. Microsoft 제공 CMake 변형의 경우 [https://github.com/Microsoft/CMake/releases](https://github.com/Microsoft/CMake/releases)에서 미리 빌드된 최신 바이너리를 다운로드합니다. 


## <a name="see-also"></a>참고 항목

[프로젝트 속성 사용](../ide/working-with-project-properties.md)<br/>
[Visual C++용 CMake 도구](../ide/cmake-tools-for-visual-cpp.md)  
