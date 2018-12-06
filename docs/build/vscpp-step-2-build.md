---
title: C + + 콘솔 앱 프로젝트 빌드 및 실행
description: 빌드 및 Visual c + +에서 Hello World 콘솔 앱 실행
ms.custom: mvc
ms.date: 12/12/2017
ms.topic: tutorial
ms.devlang: cpp
ms.assetid: 45138d71-719d-42dc-90d7-1d0ca31a2f55
ms.openlocfilehash: 09780d5823190eb4cb3b4ad13bb60e33808e4987
ms.sourcegitcommit: beeb77b2976e997debc55b1af35024cc62e62799
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/06/2018
ms.locfileid: "52977734"
---
# <a name="build-and-run-a-c-console-app-project"></a>C + + 콘솔 앱 프로젝트 빌드 및 실행

C + + 콘솔 앱 프로젝트를 만들고 코드를 입력 했을 때 빌드 수 및 Visual Studio 내에서 실행 및 명령줄에서 독립 실행형 앱으로 실행 합니다.

## <a name="prerequisites"></a>전제 조건

- 데스크톱 개발을 사용 하 여 Visual Studio를 설치 하 고 컴퓨터에서 실행 중인 c + + 워크 로드가 합니다. 아직 설치 되지 않은 경우의 단계를 따릅니다 [Visual Studio에서 c + + 설치 지원](../build/vscpp-step-0-installation.md)합니다.

- "Hello, World!" 만들기 프로젝트 및 소스 코드를 입력 합니다. 이 아직 수행 하지 않았다면의 단계를 따릅니다 [c + + 콘솔 앱 프로젝트를 만들고](../build/vscpp-step-1-create.md)합니다.

Visual Studio이 다음과 같은 경우을 빌드하고 앱을 실행 합니다.

   ![새 프로젝트를 빌드할 준비가](../build/media/vscpp-ready-to-build.png "새 프로젝트를 빌드할 준비가 되었습니다.")

## <a name="build-and-run-your-code-in-visual-studio"></a>빌드 및 Visual Studio에서 코드를 실행 합니다.

1. 프로젝트를 빌드하려면 선택 **솔루션 빌드** 에서 합니다 **빌드** 메뉴. 합니다 **출력** 창 빌드 프로세스의 결과 표시 합니다.

   ![프로젝트를 빌드할](../build/media/vscpp-build-solution.gif "프로젝트 빌드")

1. 메뉴 모음에서 코드를 실행 하려면 **디버그**하십시오 **디버깅 하지 않고 시작**합니다.

   ![프로젝트를 시작 합니다](../build/media/vscpp-start-without-debugging.gif "프로젝트 시작")

   콘솔 창이 열리고 응용 프로그램을 실행 합니다. Visual Studio에서 콘솔 앱을 시작 하면 코드를 실행 한 다음 인쇄 "계속 하려면 아무 키나 누릅니다. . ." 하면 출력을 볼 수 있도록 합니다.

지금까지 회원님이 만든 첫 번째 "Hello, world!" Visual Studio에서 콘솔 앱! 콘솔 창을 닫고 Visual Studio로 돌아와서 키를 누릅니다.

[문제를 실행 합니다.](#build-and-run-your-code-in-visual-studio-issues)

## <a name="run-your-code-in-a-command-window"></a>명령 창에서 코드를 실행 합니다.

일반적으로 Visual Studio에 없는 명령 프롬프트에서 콘솔 앱을 실행 합니다. 앱은 Visual Studio에서 빌드될 때, 모든 명령 창에서 실행할 수 있습니다. 찾기 및 명령 프롬프트 창에서 새 앱을 실행 하는 방법을 다음과 같습니다.

1. **솔루션 탐색기**, HelloWorld 솔루션을 선택 하 고 상황에 맞는 메뉴를 열려면 마우스 오른쪽 단추로 클릭 합니다. 선택 **파일 탐색기에서 폴더 열기** 여는 **파일 탐색기** HelloWorld 솔루션 폴더에는 창입니다.

1. 에 **파일 탐색기** 창 디버그 폴더를 엽니다. 이 앱, HelloWorld.exe 및 몇 개의 다른 디버깅 파일을 포함합니다. HelloWorld.exe 선택 하 고 Shift 키를 누른 상황에 맞는 메뉴를 열려면 마우스 오른쪽 단추로 클릭 합니다. 선택 **경로로 복사** 클립보드로 앱에 경로 복사 합니다.

1. 명령 프롬프트 창을 열려면 Windows-R 키를 눌러 엽니다는 **실행** 대화 합니다. 입력 *cmd.exe* 에 **열기** 텍스트 상자에 선택한 **확인** 명령 프롬프트 창을 실행 하려면.

1. 명령 프롬프트 창에서 마우스 오른쪽 단추를 앱에 경로 명령 프롬프트에 붙여 넣습니다. Enter 키를 눌러 앱을 실행 합니다.

   ![명령 프롬프트에서 앱 실행](../build/media/vscpp-run-in-cmd.gif "명령 프롬프트에서 앱을 실행 합니다.")

축, 작성 하 고 Visual Studio에서 콘솔 앱을 실행 했습니다!

[문제를 실행 합니다.](#run-your-code-in-a-command-window-issues)

## <a name="next-steps"></a>다음 단계

작성 하 고이 간단한 앱을 실행 하면, 보다 복잡 한 프로젝트에 대 한 준비가입니다. 참조 [c + + 데스크톱 개발에 Visual Studio IDE를 사용 하 여](../ide/using-the-visual-studio-ide-for-cpp-desktop-development.md) 자세한 내용을 보려면 Visual Studio에서 Visual c + +의 기능을 탐색 하는 연습입니다.

## <a name="troubleshooting-guide"></a>문제 해결 가이드

여기로 솔루션에 대 한 일반적인 문제에 첫 번째 c + + 프로젝트를 만들 때.

### <a name="build-and-run-your-code-in-visual-studio-issues"></a>빌드 및 Visual Studio 문제에서 코드를 실행 합니다.

소스 코드 편집기에 아무 것도 빨간색 물결선이 표시 하는 경우 빌드 오류 또는 경고가 있을 수 있습니다. 코드 예제에서는 대/소문자, 맞춤법 및 문장 부호에 일치 하는지 확인 합니다.

[돌아 가.](#build-and-run-your-code-in-visual-studio)

### <a name="run-your-code-in-a-command-window-issues"></a>문제 명령 창에서 코드를 실행

또한 앱을 실행 하려면 명령줄에서 디버그 솔루션 폴더를 이동할 수 있습니다. 앱에 대 한 경로 지정 하지 않고 다른 디렉터리에서 앱을 실행할 수 없습니다. 그러나 앱을 다른 디렉터리에 복사 하 고 여기에서 실행할 수 있습니다.

찾을 수 없으면 **경로로 복사** 바로 가기 메뉴에서 메뉴를 닫고 다시 여는 동안 다음 Shift 키를 누른 합니다. 이것이 단지 편의 위한입니다. 또한 파일 탐색기 검색 표시줄에서 폴더로 경로 복사 하 고 붙여 넣습니다 수는 **실행** 대화 상자에서 끝에 있는 실행 파일의 이름을 입력 합니다. 것이 좀 더 많은 입력 하지만 결과 동일 합니다.

[돌아 가.](#run-your-code-in-a-command-window)

<iframe src="" height="0" width="0" frameborder="0" name="frameTarget" />
