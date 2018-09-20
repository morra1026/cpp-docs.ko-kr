---
title: 대화 상자 클래스 만들기 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- dialog boxes [MFC], creating
- MFC dialog boxes [MFC], creating
- files [MFC], creating
- dialog classes [MFC], Add Class Wizard
- dialog classes [MFC], creating
ms.assetid: d5321741-da41-47a8-bb1c-6a0e8b28c4c1
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 9cec6ac40834e8cd3ccc9e0eadb18630ee507b92
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46442047"
---
# <a name="creating-your-dialog-class"></a>대화 상자 클래스 만들기

프로그램에서 각 대화 상자, 대화 상자 리소스를 사용 하는 새 대화 상자 클래스를 만듭니다.

[클래스 추가](../ide/adding-a-class-visual-cpp.md) 새 대화 상자 클래스를 만드는 방법에 설명 합니다. 클래스 추가 마법사를 사용 하 여 대화 상자 클래스를 만들 때 다음 항목 기록 합니다. H 및 합니다. 가 지정 하는 CPP 파일:

안에. H 파일:

- 대화 상자 클래스에 대 한 클래스 선언입니다. 클래스에서 파생 됩니다 [CDialog](../mfc/reference/cdialog-class.md)합니다.

안에. CPP 파일:

- 클래스에 대 한 메시지 맵입니다.

- 대화 상자에 대 한 표준 생성자입니다.

- 재정의 된 [DoDataExchange](../mfc/reference/cwnd-class.md#dodataexchange) 멤버 함수입니다. 이 함수를 편집 합니다. 나중에 설명 된 대로 대화 상자 데이터 교환 및 유효성 검사 기능에 사용 됩니다 [대화 상자 데이터 교환 및 유효성 검사](../mfc/dialog-data-exchange-and-validation.md)합니다.

## <a name="see-also"></a>참고 항목

[코드 마법사로 대화 상자 클래스 만들기](../mfc/creating-a-dialog-class-with-code-wizards.md)<br/>
[대화 상자의 수명 주기](../mfc/life-cycle-of-a-dialog-box.md)

