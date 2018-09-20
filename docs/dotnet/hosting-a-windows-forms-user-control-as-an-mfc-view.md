---
title: 호스트는 Windows Forms 사용자 컨트롤을 MFC 뷰로 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- MFC [C++], Windows Forms support
- Windows Forms controls [C++], hosting as an MFC view
- hosting Windows Forms control [C++]
ms.assetid: 43c02ab4-1366-434c-a980-0b19326d6ea0
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: b80b3a9d206ef48df1219d60afdc344874d3bab4
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46374518"
---
# <a name="hosting-a-windows-forms-user-control-as-an-mfc-view"></a>Windows Forms 사용자 정의 컨트롤을 MFC 뷰로 호스팅

MFC는 Windows Forms 사용자 정의 컨트롤을 MFC 뷰로에서 호스트를 CWinFormsView 클래스를 사용 합니다. MFC Windows Forms 뷰는 ActiveX 컨트롤입니다. 사용자 정의 컨트롤 기본 보기의 자식으로 호스팅되고 기본 보기의 전체 클라이언트 영역을 차지 합니다.

최종 결과 사용 되는 모델와 유사 합니다 [CFormView 클래스](../mfc/reference/cformview-class.md)합니다. 이렇게 하면 다양 한 폼 기반 보기를 만들려면 Windows Forms 디자이너 및 런타임 활용할 수 있습니다.

MFC Windows Forms 뷰는 ActiveX 컨트롤 이므로 없는 동일한 `hwnd` MFC 뷰로 합니다. 또한에 대 한 포인터를 전달할 수 없습니다는 [CView](../mfc/reference/cview-class.md) 보기. 일반적으로.NET Framework 메서드를 사용 하 여 Windows Forms 뷰를 사용 하 여 Win32에 크게 의존 합니다.

MFC를 사용 하는 Windows Forms을 보여 주는 샘플 응용 프로그램을 참조 하세요 [MFC 및 Windows Forms 통합](http://www.microsoft.com/downloads/details.aspx?FamilyID=987021bc-e575-4fe3-baa9-15aa50b0f599&displaylang=en)합니다.

## <a name="in-this-section"></a>섹션 내용

[방법: 사용자 정의 컨트롤 및 호스트 MDI 뷰 만들기](../dotnet/how-to-create-the-user-control-and-host-mdi-view.md)

[방법: Windows Forms 컨트롤에 명령 라우팅 추가](../dotnet/how-to-add-command-routing-to-the-windows-forms-control.md)

[방법: Windows Forms 컨트롤의 속성 및 메서드 호출](../dotnet/how-to-call-properties-and-methods-of-the-windows-forms-control.md)

## <a name="see-also"></a>참고 항목

[MFC에서 Windows Form 사용자 정의 컨트롤 사용](../dotnet/using-a-windows-form-user-control-in-mfc.md)<br/>
[방법: 복합 컨트롤 작성](/dotnet/framework/winforms/controls/how-to-author-composite-controls)