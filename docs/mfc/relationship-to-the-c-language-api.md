---
title: C 언어 API 관계 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
f1_keywords:
- vc.classes.mfc
dev_langs:
- C++
helpviewer_keywords:
- books [MFC], about MFC and Windows SDK
- books [MFC]
- MFC, Windows API
- Visual C, Windows API calls
- Windows API [MFC], and MFC
ms.assetid: 334e8efc-f3cc-4018-bc2e-02908b2a39fe
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 027a14213f173bdc6be5fc34e9fd4faf0eba8023
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46415156"
---
# <a name="relationship-to-the-c-language-api"></a>C 언어 API와의 관계

Windows에 대 한 다른 클래스 라이브러리 외에도 Microsoft Foundation 클래스 (MFC) 라이브러리를 설정 하는 단일 특성은 C 언어로 작성 된 Windows API에 근접 매핑은. 또한 혼합할 수 있습니다 일반적으로 클래스 라이브러리에 대 한 호출 자유롭게 Windows API를 직접 호출 합니다. 하지만 이러한 직접 액세스 의미 하지 않습니다, 해당 API에 대 한 완전 한 대체 클래스는. 개발자 해야 같은 일부 Windows 함수를 직접 호출을 수행할 종종 [SetCursor](/windows/desktop/api/winuser/nf-winuser-setcursor) 하 고 [GetSystemMetrics](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)예를 들어 합니다. Windows 함수 분명 한 이점은 이렇게 하는 경우에 클래스 멤버 함수에 의해 래핑됩니다.

경우에 따라 네이티브 Windows 함수 호출을 수행 해야 하기 때문에 C 언어 Windows API 설명서에 대 한 액세스를 해야 합니다. 이 설명서는 Microsoft Visual c + +를 사용 하 여 포함 합니다.

> [!NOTE]
>  MFC 라이브러리 프레임 워크의 작동 방식 개요를 참조 하세요 [클래스를 사용 하 여 Windows에 대 한 응용 프로그램 작성을](../mfc/using-the-classes-to-write-applications-for-windows.md)입니다.

## <a name="see-also"></a>참고 항목

[일반 클래스 디자인 원칙](../mfc/general-class-design-philosophy.md)
