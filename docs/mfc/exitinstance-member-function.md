---
title: ExitInstance 멤버 함수 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
f1_keywords: []
dev_langs:
- C++
helpviewer_keywords:
- programs [MFC], terminating
- CWinApp class [MFC], ExitInstance
- ExitInstance method [MFC]
ms.assetid: 5bb597bd-8dab-4d49-8bcf-9c45aa8be4a2
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: da411fbecdea0a1e7b8976ca119057204693a9bd
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46387863"
---
# <a name="exitinstance-member-function"></a>ExitInstance 멤버 함수

합니다 [ExitInstance](../mfc/reference/cwinapp-class.md#exitinstance) 클래스의 멤버 함수 [CWinApp](../mfc/reference/cwinapp-class.md) 응용 프로그램의 복사본으로 종료 되 면 일반적으로 응용 프로그램을 종료 하는 사용자의 결과로 때마다 호출 됩니다.

재정의 `ExitInstance` 그래픽 장치 GDI (인터페이스) 리소스를 해제 또는 프로그램 실행 중에 사용 되는 메모리 할당 해제와 같은 특별 한 정리 처리 해야 합니다. 그러나 문서 및 뷰과 같은 표준 항목의 정리는 해당 개체에 특정 특별 한 정리를 수행 하기 위한 다른 재정의 가능 함수를 사용 하 여 framework에서 제공 됩니다.

## <a name="see-also"></a>참고 항목

[CWinApp: 응용 프로그램 클래스](../mfc/cwinapp-the-application-class.md)
