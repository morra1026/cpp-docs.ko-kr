---
title: DLL의 자동화 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- DLLs [C++], Automation
- Automation [C++], DLLs
ms.assetid: 2728ecd1-14e2-4ae0-a946-e749e11dbb74
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: cde5d0e400f1bdd3f5a851d47da581380273b04a
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45717786"
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