---
title: 프레임 워크의 대화 상자 구성 요소 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- MFC dialog boxes [MFC], creating
- dialog classes [MFC], dialog box components
- MFC dialog boxes [MFC], about MFC dialog boxes
- dialog templates [MFC], MFC framework
- MFC dialog boxes [MFC], dialog resource
ms.assetid: 592db160-0a8a-49be-ac72-ead278aca53f
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 6936a48d1a3e1845d56c73524c84800d9d605155
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50065514"
---
# <a name="dialog-box-components-in-the-framework"></a>프레임워크의 대화 상자 구성 요소

MFC 프레임 워크 대화 상자에는 두 가지 구성 요소:

- 대화 상자의 컨트롤 및 배치를 지정 하는 대화 상자 템플릿 리소스입니다.

   대화 상자 리소스는 Windows 대화 상자 창을 만들고 표시 대화 상자 템플릿을 저장 합니다. 템플릿 크기, 위치, 스타일 및 형식 및 대화 상자의 컨트롤의 위치를 포함 하 여 대화 상자의 특성을 지정 합니다. 일반적으로 리소스로 저장 대화 상자 템플릿을 사용할 하지만 메모리에서 사용자 고유의 템플릿을 만들 수도 있습니다.

- 대화 상자 클래스에서 파생 [CDialog](../mfc/reference/cdialog-class.md), 대화 상자를 관리 하기 위한 프로그래밍 인터페이스를 제공 합니다.

   대화 상자는 창 및 표시 될 때 Windows 창을에 연결 됩니다. 대화 상자 창 만들어지면 대화 상자 템플릿 리소스 자식 대화 상자 창 컨트롤을 만들기 위한 템플릿으로 사용 됩니다.

## <a name="see-also"></a>참고 항목

[대화 상자](../mfc/dialog-boxes.md)<br/>
[대화 상자의 수명 주기](../mfc/life-cycle-of-a-dialog-box.md)

