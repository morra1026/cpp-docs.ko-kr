---
title: 다중 스레드 프로그램
ms.date: 11/04/2016
helpviewer_keywords:
- threading [C++], about threading
- multithreading [C++], about threads
ms.assetid: 02443596-f7e1-48d0-b3a4-39ee0e54e444
ms.openlocfilehash: 0b79fe84fbf7d910d53cb5bc333668b7d99ab8ae
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50502046"
---
# <a name="multithread-programs"></a>다중 스레드 프로그램

스레드는 기본적으로 프로그램을 통해 실행 경로입니다. Win32 예약 된 실행의 최소 단위 이기도 합니다. CPU 레지스터 및 시스템 스케줄러가 실행 목록에서 항목의 상태는 스택, 스레드 구성 됩니다. 각 스레드는 프로세스의 모든 리소스를 공유합니다.

하나 이상의 스레드가 코드, 데이터 및 메모리에 있는 프로그램의 다른 리소스의 프로세스 구성 됩니다. 일반적인 프로그램 리소스는 열려 있는 파일, 세마포 및 동적으로 할당 된 메모리입니다. 프로그램에는 자체 스레드 중 하나 시스템 스케줄러가 실행 제어를 제공 하는 제공 하는 경우 실행 합니다. 스케줄러는 스레드 실행 해야 하며 실행 시기를 결정 합니다. 우선 순위가 낮은 스레드 우선 순위가 높은 스레드가 작업을 완료할 때 대기 해야 합니다. 다중 프로세서 컴퓨터에서 스케줄러 CPU 부하를 분산 하는 다른 프로세서에 개별 스레드를 이동할 수 있습니다.

각 스레드는 프로세스에서 독립적으로 작동 합니다. 하지 않을 경우에 서로 표시, 스레드 개별적으로 실행 하 고 다른 스레드와 프로세스에서 인식 되지 않습니다. 그러나 공용 리소스를 공유 하는 스레드가 세마포 또는 프로세스 간 통신의 다른 메서드를 사용 하 여 작업을 조정 해야 합니다. 스레드를 동기화 하는 방법에 대 한 자세한 내용은 참조 하세요. [다중 스레드 Win32 프로그램 작성](writing-a-multithreaded-win32-program.md)합니다.

## <a name="see-also"></a>참고 항목

[C 및 Win32를 사용한 다중 스레딩](multithreading-with-c-and-win32.md)