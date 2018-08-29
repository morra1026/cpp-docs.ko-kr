---
title: 다중 스레드 프로그램으로 문제 영역 방지 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- multithreading [C++], troubleshooting
- errors [C++], multithreaded programs
- threading [C++], troubleshooting
- troubleshooting [C++], multithreading
ms.assetid: 06cc231d-bb5a-409d-8bd3-676c9e2a8c5b
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 97a69c52adb5094c7c7841a93b73b1a83cd786d9
ms.sourcegitcommit: f7703076b850c717c33d72fb0755fbb2215c5ddc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/28/2018
ms.locfileid: "43131064"
---
# <a name="avoiding-problem-areas-with-multithread-programs"></a>다중 스레드 프로그램으로 문제 영역 방지
만들기, 링크 또는 다중 스레드 C 프로그램을 실행할 때 발생할 수 있는 몇 가지 문제가 있습니다. 다음 표에 일반적인 문제 설명 되어 있습니다. (MFC의 관점에서 유사한 내용은 참조 하세요. [다중 스레딩: 프로그래밍 팁](multithreading-programming-tips.md).)  
  
|문제점|가능한 원인|  
|-------------|--------------------|  
|프로그램 보호 위반으로 인해 되었음을 보여 주는 메시지 상자를 표시 합니다.|많은 Win32 프로그래밍 오류로 인해 보호 위반이 발생 합니다. 보호 위반을 일반적인 원인은 간접 할당 데이터 null 포인터를 사용 하는 것입니다. 이 식의 결과에 속하지 않는 메모리에 액세스 하려고 하는 프로그램에서 때문에 보호 위반이 발생 합니다.<br /><br /> 보호 위반의 원인을 파악 하는 간편한 방법은 디버깅 정보를 사용 하 여 프로그램을 컴파일하면 다음 Visual c + + 환경에서 디버거를 통해 실행 하는 경우 보호 오류가 발생 하면 Windows 디버거에 제어를 전송 하 고 문제의 원인이 된 줄에 커서가 놓입니다.|  
|프로그램 다양 한 컴파일 및 링크 오류를 생성합니다.|가장 높은 값 중 하나에 컴파일러의 경고 수준을 설정 하 고 경고 메시지에 주의 하 여 여러 가지 잠재적인 문제를 제거할 수 있습니다. 3 수준 또는 수준 4 경고 수준 옵션을 사용 하 여 의도 하지 않은 데이터 변환, 누락 된 함수 프로토타입 및 ansi 형식이 아닌 기능의 사용을 검색할 수 있습니다.|  
  
## <a name="see-also"></a>참고 항목  

[C 및 Win32를 사용한 다중 스레딩](multithreading-with-c-and-win32.md)