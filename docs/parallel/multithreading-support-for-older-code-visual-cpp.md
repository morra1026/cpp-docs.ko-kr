---
title: 이전 코드를 위한 다중 스레드 지원(Visual C++)
ms.date: 08/27/2018
helpviewer_keywords:
- threading [C++]
- multiple threads
- concurrent programming [C++]
- programming [C++], multithreaded
- multithreading [C++], about multithreading
- multiple concurrent threads
- multithreading [C++]
ms.assetid: 24425b1f-5031-4c6b-aac7-017115a40e7c
ms.openlocfilehash: 649e26c3f0704dfd6740b1a250613545e29316a3
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50457735"
---
# <a name="multithreading-support-for-older-code-visual-c"></a>이전 코드를 위한 다중 스레드 지원(Visual C++)

Visual c + +를 사용 하면 여러 동시 실행 스레드를 동시에 실행할 수 있습니다. 사용 하 여 다중 스레딩, 백그라운드 작업 분리 시키고 동시 입력 스트림을 관리, 사용자 인터페이스 등을 관리할 수 있습니다.

## <a name="in-this-section"></a>섹션 내용

[C 및 Win32를 사용한 다중 스레딩](multithreading-with-c-and-win32.md)<br/>
Microsoft Windows를 사용 하 여 다중 스레드 응용 프로그램 만들기에 대 한 지원 제공

[C++ 및 MFC에서 다중 스레딩](multithreading-with-cpp-and-mfc.md)<br/>
프로세스 및 스레드 이란 무엇 이며 MFC에 접근 하는 방법에 대해 설명 합니다. 다중 스레딩 됩니다.

[다중 스레딩 및 로캘](multithreading-and-locales.md)<br/>
C 런타임 라이브러리와 다중 스레드 응용 프로그램에서 c + + 표준 라이브러리의 로캘 기능을 사용 하는 경우 발생 하는 문제를 설명 합니다.

## <a name="related-sections"></a>관련 단원

[CWinThread](../mfc/reference/cwinthread-class.md)<br/>
응용 프로그램 내의 실행 스레드를 나타냅니다.

[CSyncObject](../mfc/reference/csyncobject-class.md)<br/>
Win32의 동기화 개체에 공통 기능을 제공 하는 순수 가상 클래스를 설명 합니다.

[CSemaphore](../mfc/reference/csemaphore-class.md)<br/>
하나 이상의 프로세스가 리소스에 액세스할 수에 제한 된 수의 스레드를 허용 하는 동기화 개체인 세마포를 나타냅니다.

[CMutex](../mfc/reference/cmutex-class.md)<br/>
한 스레드가 한 리소스에 상호 배타적으로 액세스하도록 허용하는 동기화 개체인 뮤텍스를 나타냅니다.

[CCriticalSection](../mfc/reference/ccriticalsection-class.md)<br/>
리소스 또는 코드 섹션에 액세스 하는 한 번에 하나의 스레드를 허용 하는 동기화 개체인 중요 섹션을 나타냅니다.

[CEvent](../mfc/reference/cevent-class.md)<br/>
한 스레드가 다른 이벤트가 발생 했음을 알리도록 허용 하는 동기화 개체인 이벤트를 나타냅니다.

[CMultiLock](../mfc/reference/cmultilock-class.md)<br/>
다중 스레드 프로그램에 대한 액세스를 제어할 때 사용하는 액세스 제어 메커니즘을 나타냅니다.

[CSingleLock](../mfc/reference/csinglelock-class.md)<br/>
다중 스레드 프로그램에서 한 리소스에 대한 액세스를 제어할 때 사용하는 액세스 제어 메커니즘을 나타냅니다.