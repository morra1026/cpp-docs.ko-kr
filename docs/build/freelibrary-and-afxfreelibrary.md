---
title: FreeLibrary 및 AfxFreeLibrary
ms.date: 11/04/2016
f1_keywords:
- FreeLibrary
- AfxFreeLibrary
helpviewer_keywords:
- extension DLLs [C++], unloading
- AfxFreeLibrary method
- unloading DLLs
- FreeLibrary method
- DLLs [C++], linking
- explicit linking [C++]
- DLLs [C++], unloading
ms.assetid: 4a48d290-3971-43e9-8e97-ba656cd0c8f8
ms.openlocfilehash: ce52eb43fa8f371b68d836f01163003f056f34c7
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50530236"
---
# <a name="freelibrary-and-afxfreelibrary"></a>FreeLibrary 및 AfxFreeLibrary

DLL 호출에 명시적으로 연결 하는 프로세스를 [FreeLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary) DLL 모듈이 더 이상 필요 없는 경우에 작동 합니다. 이 함수는 모듈의 참조 횟수를 프로세스의 주소 공간에서 참조 횟수가 0 이면 매핑을 해제 합니다.

MFC 응용 프로그램에서 사용 하 여 [AfxFreeLibrary](../mfc/reference/application-information-and-management.md#afxfreelibrary) 대신 `FreeLibrary` MFC 확장 DLL을 언로드할 수 있습니다. 인터페이스 (함수 프로토타입)에 대 한 `AfxFreeLibrary` 같습니다 `FreeLibrary`합니다.

## <a name="what-do-you-want-to-do"></a>원하는 작업을 선택하세요.

- [DLL에 암시적으로 연결 하는 방법](../build/linking-an-executable-to-a-dll.md#linking-implicitly)

- [사용할 링크 방법 결정](../build/linking-an-executable-to-a-dll.md#determining-which-linking-method-to-use)

## <a name="what-do-you-want-to-know-more-about"></a>추가 정보

- [LoadLibrary 및 AfxLoadLibrary](../build/loadlibrary-and-afxloadlibrary.md)

- [GetProcAddress](../build/getprocaddress.md)

## <a name="see-also"></a>참고 항목

[Visual C++의 DLL](../build/dlls-in-visual-cpp.md)<br/>
[FreeLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary)
[AfxFreeLibrary](../mfc/reference/application-information-and-management.md#afxfreelibrary)