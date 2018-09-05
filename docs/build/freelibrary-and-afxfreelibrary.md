---
title: FreeLibrary 및 AfxFreeLibrary | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
f1_keywords:
- FreeLibrary
- AfxFreeLibrary
dev_langs:
- C++
helpviewer_keywords:
- extension DLLs [C++], unloading
- AfxFreeLibrary method
- unloading DLLs
- FreeLibrary method
- DLLs [C++], linking
- explicit linking [C++]
- DLLs [C++], unloading
ms.assetid: 4a48d290-3971-43e9-8e97-ba656cd0c8f8
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 063c858253c12cfedbf252a124029b8cbc16a691
ms.sourcegitcommit: a7046aac86f1c83faba1088c80698474e25fe7c3
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43680965"
---
# <a name="freelibrary-and-afxfreelibrary"></a>FreeLibrary 및 AfxFreeLibrary
DLL 호출에 명시적으로 연결 하는 프로세스를 [FreeLibrary](https://msdn.microsoft.com/library/windows/desktop/ms683152(v=vs.85).aspx) DLL 모듈이 더 이상 필요 없는 경우에 작동 합니다. 이 함수는 모듈의 참조 횟수를 프로세스의 주소 공간에서 참조 횟수가 0 이면 매핑을 해제 합니다.  
  
 MFC 응용 프로그램에서 사용 하 여 [AfxFreeLibrary](../mfc/reference/application-information-and-management.md#afxfreelibrary) 대신 `FreeLibrary` MFC 확장 DLL을 언로드할 수 있습니다. 인터페이스 (함수 프로토타입)에 대 한 `AfxFreeLibrary` 같습니다 `FreeLibrary`합니다.  
  
## <a name="what-do-you-want-to-do"></a>원하는 작업을 선택하세요.  
  
-   [DLL에 암시적으로 연결 하는 방법](../build/linking-an-executable-to-a-dll.md#linking-implicitly)  
  
-   [사용할 링크 방법 결정](../build/linking-an-executable-to-a-dll.md#determining-which-linking-method-to-use)  
  
## <a name="what-do-you-want-to-know-more-about"></a>추가 정보  
  
-   [LoadLibrary 및 AfxLoadLibrary](../build/loadlibrary-and-afxloadlibrary.md)  
  
-   [GetProcAddress](../build/getprocaddress.md)  
  
## <a name="see-also"></a>참고 항목  
 [Visual c + + Dll](../build/dlls-in-visual-cpp.md)   
 [FreeLibrary](https://msdn.microsoft.com/library/windows/desktop/ms683152(v=vs.85).aspx)   
 [AfxFreeLibrary](../mfc/reference/application-information-and-management.md#afxfreelibrary)