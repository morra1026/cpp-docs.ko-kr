---
title: Visual Studio에서 CMake 디버깅 세션 구성
ms.date: 03/05/2019
helpviewer_keywords:
- CMake debugging
ms.openlocfilehash: 9a4dd009544a4590c336697ba2162eec45718869
ms.sourcegitcommit: 8105b7003b89b73b4359644ff4281e1595352dda
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57827927"
---
# <a name="configure-cmake-debugging-sessions"></a>CMake 디버깅 세션 구성

실행 가능한 모든 CMake 대상은 **일반** 도구 모음의 **시작 항목** 드롭다운에 표시됩니다. 디버깅 세션을 시작하려면 하나를 선택하고 디버거를 시작하기만 하면 됩니다.

![CMake 시작 항목 드롭다운](media/cmake-startup-item-dropdown.png "CMake 시작 항목 드롭다운")

CMake 메뉴에서 디버그 세션을 시작할 수도 있습니다.

## <a name="customize-debugger-settings"></a>디버거 설정 사용자 지정

프로젝트의 실행 가능한 CMake 대상에 대한 디버거 설정을 사용자 지정하려면, 특정 CMakeLists.txt 파일을 마우스 오른쪽 단추로 클릭하고 **디버그 및 시작 설정**을 선택합니다. 하위 메뉴에서 CMake 대상을 선택하면 `launch.vs.json`이라는 파일이 만들어집니다. 이 파일은 선택한 CMake 대상에 대한 정보로 미리 채워져 있으며 프로그램 인수자 또는 디버거 형식과 같은 추가 매개 변수를 지정할 수 있습니다. `CMakeSettings.json` 파일의 모든 키를 참조하려면 `launch.vs.json`에 `cmake.`로 서문을 작성합니다. 다음 예제에서는 현재 선택된 구성에 대한 `CMakeSettings.json` 파일에서 `remoteCopySources` 키 값을 가져오는 간단한 `launch.vs.json` 파일을 보여줍니다.

```json
{
  "version": "0.2.1",
  "defaults": {},
  "configurations": [
    {
      "type": "default",
      "project": "CMakeLists.txt",
      "projectTarget": "CMakeHelloWorld.exe (Debug\\CMakeHelloWorld.exe)",
      "name": "CMakeHelloWorld.exe (Debug\\CMakeHelloWorld.exe)",
      "args": ["${cmake.remoteCopySources}"]
    }
  ]
}
```

`launch.vs.json` 파일을 저장하는 즉시 **시작 항목** 드롭다운에 새 이름의 항목이 만들어집니다. `launch.vs.json` 파일을 편집하여 임의 개수의 CMake 대상에 대해 원하는 만큼 많은 디버그 구성을 만들 수 있습니다.

## <a name="support-for-cmakesettings-variables"></a>CMakeSettings 변수 지원

 `Launch.vs.json`은 `CMakeSettings.json`(아래 참조)에서 선언되고 현재 선택한 구성에 적용된 변수를 지원합니다. 또한 시작하는 앱의 현재 디렉터리를 설정하는 `currentDir`이라는 키가 있습니다.

```json
{
  "type": "default",
  "project": "CMakeLists.txt",
  "projectTarget": "CMakeHelloWorld1.exe (C:\\Users\\satyan\\CMakeBuilds\\Test\\Debug\\CMakeHelloWorld1.exe)",
  "name": "CMakeHelloWorld1.exe (C:\\Users\\satyan\\CMakeBuilds\\Test\\Debug\\CMakeHelloWorld1.exe)",
  "currentDir": "${env.USERPROFILE}\\CMakeBuilds\\${workspaceHash}"
}
```

응용 프로그램을 실행할 때 `currentDir` 값은 다음과 비슷합니다.

```cmd
C:\Users\satyan\7f14809a-2626-873e-952e-cdf038211175\
```
## <a name="see-also"></a>참고자료

[Visual Studio의 CMake 프로젝트](cmake-projects-in-visual-studio.md)<br/>
[Linux CMake 프로젝트 구성](../linux/cmake-linux-project.md)<br/>
[원격 Linux 컴퓨터에 연결](../linux/connect-to-your-remote-linux-computer.md)<br/>
[CMake 빌드 설정 사용자 지정](customize-cmake-settings.md)<br/>
[CMake 디버깅 세션 구성](configure-cmake-debugging-sessions.md)<br/>
[Linux 프로젝트 배포, 실행 및 디버그](../linux/deploy-run-and-debug-your-linux-project.md)<br/>
[CMake 미리 정의된 구성 참조](cmake-predefined-configuration-reference.md)<br/>