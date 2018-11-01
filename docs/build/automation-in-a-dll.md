---
title: DLL의 자동화
ms.date: 11/04/2016
helpviewer_keywords:
- DLLs [C++], Automation
- Automation [C++], DLLs
ms.assetid: 2728ecd1-14e2-4ae0-a946-e749e11dbb74
ms.openlocfilehash: b9d4f7a71ceb384069fcbef6bf791f0c5fd1b933
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50536541"
---
# <a name="automation-in-a-dll"></a>DLL의 자동화

MFC DLL 마법사에서 자동화 옵션을 선택 하면 마법사는 다음을 사용 하 여 제공.

- 시작 개체 설명 언어 (합니다. ODL) 파일

- Afxole.h STDAFX.h 파일에 include 지시문

- 구현의 합니다 `DllGetClassObject` 함수를 호출 합니다 **AfxDllGetClassObject** 함수

- 구현의 합니다 `DllCanUnloadNow` 함수를 호출 합니다 **AfxDllCanUnloadNow** 함수

- 구현의 합니다 `DllRegisterServer` 함수를 호출 합니다 [등록 됩니다](../mfc/reference/coleobjectfactory-class.md#updateregistryall) 함수

## <a name="what-do-you-want-to-know-more-about"></a>추가 정보

- [자동화 서버](../mfc/automation-servers.md)

## <a name="see-also"></a>참고 항목

[Visual C++의 DLL](../build/dlls-in-visual-cpp.md)