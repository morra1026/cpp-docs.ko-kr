---
title: 문서 템플릿 및 문서-뷰 만들기 프로세스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- icons, for multiple document templates
- document templates [MFC], and views
- document/view architecture [MFC], creating document/view
- single document template
- MFC, document templates
- multiple document template
- CDocTemplate class [MFC]
- templates [MFC], document templates
ms.assetid: 311ce4cd-fbdf-4ea1-a51b-5bb043abbcee
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 182cf58b3ee712ef0d45719591e967c0b81909bd
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46426525"
---
# <a name="document-templates-and-the-documentview-creation-process"></a>문서 템플릿 및 문서/뷰 만들기 프로세스

프레임 워크의 두 문서 템플릿 클래스는 프레임 창와 연결 된 뷰를 사용 하 여 문서를 만드는 복잡 한 프로세스를 관리 하려면: [CSingleDocTemplate](../mfc/reference/csingledoctemplate-class.md) SDI 응용 프로그램 및 [CMultiDocTemplate ](../mfc/reference/cmultidoctemplate-class.md) MDI 응용 프로그램에 대 한 합니다. `CSingleDocTemplate` 만들고 한 번에 한 가지 유형의 하나의 문서를 저장할 수 있습니다. `CMultiDocTemplate` 열려 있는 문서의 다양 한 형식의 목록을 유지 합니다.

일부 응용 프로그램에는 여러 문서 유형을 지원 합니다. 예를 들어, 응용 프로그램은 텍스트 문서 및 그래픽 문서 지원할 수 있습니다. 이러한 응용 프로그램에서 사용자가 파일 메뉴에서 새 명령을 선택할 때 대화 상자에는 가능한 형식의 새 문서를 열려면 목록을 표시 합니다. 각 지원 되는 문서 형식에 대 한 응용 프로그램에 고유한 문서 템플릿 개체를 사용합니다. 다음 그림에서는 두 문서 형식을 지원 하며, 여러 열린 문서를 표시 하는 MDI 응용 프로그램의 구성을 보여 줍니다.

![두 가지 문서 형식이 포함 된 MDI 응용 프로그램](../mfc/media/vc387h1.gif "vc387h1") 두 문서 형식을 사용 하 여 MDI 응용 프로그램

문서 템플릿 생성 및 응용 프로그램 개체에서 유지 관리 됩니다. 주요 작업 중 하나를 수행할 응용 프로그램 중 `InitInstance` 기능은 적절 한 종류의 하나 이상의 문서 템플릿이 생성 하는 것입니다. 이 기능에 설명 되어 [문서 템플릿 만들기](../mfc/document-template-creation.md)합니다. 응용 프로그램 개체 템플릿 목록에서 각 서식 파일에 대 한 포인터를 저장 하 고 문서 템플릿을 추가 하는 인터페이스를 제공 합니다.

두 개 이상의 문서 형식을 지원 해야 하는 경우에를 추가로 호출을 추가 해야 합니다 [AddDocTemplate](../mfc/reference/cwinapp-class.md#adddoctemplate) 각 문서 유형에 대 한 합니다.

아이콘은 응용 프로그램의 목록에서 문서 템플릿의 해당 위치에 따라 각 문서 서식 파일에 등록 됩니다. 문서 서식 파일의 순서를 호출 하 여 추가 되는 순서에 따라 결정 됩니다 `AddDocTemplate`합니다. MFC는 응용 프로그램의 첫 번째 아이콘 리소스는 응용 프로그램 아이콘, 다음 아이콘 리소스는 첫 번째 문서 아이콘을 가정 합니다.

예를 들어, 문서 템플릿은 응용 프로그램에 대 한 세 가지 중 세 번째입니다. 인덱스 3에 응용 프로그램의 아이콘 리소스를 문서 템플릿에 대 한 해당 아이콘이 사용 됩니다. 그렇지 않은 경우 인덱스 0에 있는 아이콘을 기본으로 사용 됩니다.

## <a name="see-also"></a>참고 항목

[일반 MFC 항목](../mfc/general-mfc-topics.md)<br/>
[문서 템플릿 만들기](../mfc/document-template-creation.md)<br/>
[문서/뷰 만들기](../mfc/document-view-creation.md)<br/>
[MFC 개체 간 관계](../mfc/relationships-among-mfc-objects.md)<br/>
[새 문서, 창 및 뷰 만들기](../mfc/creating-new-documents-windows-and-views.md)

