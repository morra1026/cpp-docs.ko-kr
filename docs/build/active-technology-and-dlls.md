---
title: 액티브 기술 및 DLL
ms.date: 11/04/2016
helpviewer_keywords:
- in-process server DLLs
- Automation [C++], DLLs
- DLLs [C++], Active Technology
- Active technology [C++]
- MFC DLLs [C++], Active Technology
ms.assetid: 3ed27f8d-164a-4562-ad61-9f2333404cc7
ms.openlocfilehash: 270c64df9af792a73acf1ad408aca02e7fadc30f
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50535813"
---
# <a name="active-technology-and-dlls"></a>액티브 기술 및 DLL

액티브 기술 개체 서버를 DLL 내에서 완전히 구현 될 수 있습니다. 이 유형의 서버를 in-process 서버를 라고 합니다. MFC 지원 하지 않습니다 완전히 in-process 서버 비주얼 편집의 모든 기능에 대 한 액티브 기술 컨테이너의 기본 메시지 루프에 연결할 서버에 대 한 방법을 제공 하지 않습니다 하기 쉽다는 이유. MFC는 액셀러레이터 키 및 유휴 시간 처리를 처리 하는 컨테이너 응용 프로그램의 메시지 루프에 대 한 액세스를 해야 합니다.

사용자 인터페이스가 없는 자동화 서버를 작성하는 경우에는 해당 서버를 in-process 서버로 만든 다음 DLL에 완전히 포함시킬 수 있습니다.

## <a name="what-do-you-want-to-know-more-about"></a>추가 정보

- [자동화 서버](../mfc/automation-servers.md)

## <a name="see-also"></a>참고 항목

[Visual C++의 DLL](../build/dlls-in-visual-cpp.md)