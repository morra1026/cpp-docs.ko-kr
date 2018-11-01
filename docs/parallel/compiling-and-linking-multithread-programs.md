---
title: 다중 스레드 프로그램 컴파일 및 링크
ms.date: 11/04/2016
helpviewer_keywords:
- compiling multithreaded programs
- multithreading [C++], linking programs
- threading [C++], linking programs
- multithreading [C++], compiled programs
- threading [C++], compiled programs
- compiling source code [C++], multithread programs
- linking [C++], multithread programs
ms.assetid: 27589afc-daf2-4f26-b868-a99de5c9dfec
ms.openlocfilehash: 3d98f5341de1374c9119e2a4303c94fcfb005e29
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50558888"
---
# <a name="compiling-and-linking-multithread-programs"></a>다중 스레드 프로그램 컴파일 및 링크

Bounce.c 프로그램에 도입 되어 [샘플 다중 스레드 C 프로그램](sample-multithread-c-program.md)합니다.

프로그램을 컴파일되지 기본적으로 다중 스레드입니다.

### <a name="to-compile-and-link-the-multithread-program-bouncec-from-within-the-development-environment"></a>컴파일 및 개발 환경 내에서 Bounce.c 다중 스레드 프로그램을 연결 하려면

1. **파일** 메뉴에서 **새로 만들기**를 클릭한 다음 **프로젝트**를 클릭합니다.

1. 에 **프로젝트 형식** 창 클릭 **Win32**합니다.

1. 에 **템플릿을** 창 클릭 **Win32 콘솔 응용 프로그램**, 한 다음 프로젝트의 이름을 합니다.

1. 프로젝트에 C 소스 코드를 포함 하는 파일을 추가 합니다.

1. 에 **빌드** 메뉴를 클릭 하 여 프로젝트를 빌드합니다 합니다 **빌드** 명령.

### <a name="to-compile-and-link-the-multithread-program-bouncec-from-the-command-line"></a>컴파일하고 Bounce.c 명령줄에서 다중 스레드 프로그램을 연결 하려면

1. 컴파일하고 프로그램을 링크 합니다.

    ```
    CL BOUNCE.C
    ```

## <a name="see-also"></a>참고 항목

[C 및 Win32를 사용한 다중 스레딩](multithreading-with-c-and-win32.md)