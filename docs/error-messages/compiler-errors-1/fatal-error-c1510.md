---
title: 심각한 오류 C1510 | Microsoft Docs
ms.custom: ''
ms.date: 04/11/2017
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C1510
dev_langs:
- C++
helpviewer_keywords:
- C1510
ms.assetid: 150c827f-9514-41a9-8d7e-82f820749bcb
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 25b1c3f83b770dc7b346e83e9675afe423af2516
ms.sourcegitcommit: a41c4d096afca1e9b619bbbce045b77135d32ae2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/14/2018
ms.locfileid: "42541883"
---
# <a name="fatal-error-c1510"></a>심각한 오류 C1510
언어 리소스 clui.dll을 열 수 없습니다.  
  
 컴파일러는 언어 리소스 DLL을 로드할 수 없습니다.  
  
이 문제에 대 한 공통적인 두 원인이 있습니다. 32 비트 컴파일러 및 도구를 사용 하는 경우 링크 중 2GB 이상의 메모리를 사용 하는 대규모 프로젝트에 대 한이 오류가 표시 될 수 있습니다. 64 비트 Windows 시스템에서 사용 가능한 해결 크로스 컴파일러 및 코드 생성 도구 또는 64 비트 네이티브를 사용 하는 것입니다. 이 64 비트 응용 프로그램을 사용할 수 있는 더 큰 메모리 공간 활용 합니다. 32 비트 시스템에서 실행 되므로 32 비트 컴파일러를 사용 해야 하는 경우에 따라서는 링커 3GB를 사용할 수 있는 메모리의 양을 늘릴 수 있습니다. 자세한 내용은 참조 하세요. [4gb 튜닝: BCDEdit 및 Boot.ini](https://msdn.microsoft.com/library/vs/alm/bb613473\(v=vs.85\).aspx) 하며 [BCDEdit increaseuserva 설정](https://msdn.microsoft.com/library/ff542202.aspx) 명령입니다.  

다른 일반적인 원인은 손상 되었거나 불완전 한 Visual Studio 설치 합니다. 이 경우 설치 관리자를 복구 하거나 Visual Studio를 다시 설치를 다시 실행 합니다.  
  