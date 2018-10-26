---
title: 프로젝트에 폼 삽입 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- inserting forms [MFC]
- Insert New dialog box [MFC]
- forms, adding to projects
ms.assetid: f3bd2998-3ce2-496d-ac5c-57ca70eec7cb
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: ba22c87ee601d66ccfb1092047e69be42d8163c3
ms.sourcegitcommit: a9dcbcc85b4c28eed280d8e451c494a00d8c4c25
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/25/2018
ms.locfileid: "50052757"
---
# <a name="inserting-a-form-into-a-project"></a>프로젝트에 폼 삽입

폼은 컨트롤에 대 한 편리한 컨테이너를 제공합니다. 응용 프로그램이 MFC 라이브러리 지원으로 응용 프로그램에 MFC 기반 폼을 삽입할 수 있습니다.

### <a name="to-insert-a-form-into-your-project"></a>프로젝트에 폼 삽입 하려면

1. 클래스 뷰에서 폼을 추가할 프로젝트를 선택 하 고 마우스 오른쪽 단추를 클릭 합니다.

1. 바로 가기 메뉴에서 클릭 **추가** 을 클릭 한 다음 **클래스 추가**합니다.

   경우는 **새 폼** 명령을 사용할 수 없는, 프로젝트에 활성 템플릿 라이브러리 (ATL)에 기반 할 수 있습니다. ATL 프로젝트에 폼을 추가 하려면 [설정이 지정](../atl/reference/application-settings-atl-project-wizard.md) 먼저 프로젝트를 만들 때.

1. **MFC** 폴더를 클릭 **MFC 클래스**합니다.

1. MFC 클래스 마법사를 사용 하 여 새 클래스에서 파생 수행해 [CFormView](../mfc/reference/cformview-class.md)합니다.

Visual c + + 폼에 추가 응용 프로그램을 시작할 수 있도록 대화 상자 편집기에서 열고 컨트롤 추가 및 전반적인 디자인에서 작동 합니다.

(대화 상자 기반 응용 프로그램에는 적용 되지 않음) 다음과 같은 추가 단계를 수행 하는 것이 좋습니다.

1. 재정의 `OnUpdate` 멤버 함수입니다.

1. 문서 보기에서 데이터를 이동 하는 멤버 함수를 구현 합니다.

1. 만들기는 `OnPrint` 멤버 함수입니다.

## <a name="see-also"></a>참고 항목

[폼 뷰](../mfc/form-views-mfc.md)

