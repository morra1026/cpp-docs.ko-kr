---
title: MFC의 OLE | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- MFC, OLE and
- OLE items
- OLE applications [MFC], about OLE
- OLE [MFC]
- OLE containers [MFC], about OLE
- applications [OLE], about OLE
- OLE component object model (COM)
ms.assetid: 5193479d-1239-4697-aea4-e82f92c707ab
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: c6c39c47762f4ac61e3192d5d3ecef997c3078bc
ms.sourcegitcommit: 9a0905c03a73c904014ec9fd3d6e59e4fa7813cd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/29/2018
ms.locfileid: "43204116"
---
# <a name="ole-in-mfc"></a>MFC의 OLE
이 문서에서는 MFC를 사용 하 여 OLE 프로그래밍의 기본적인 사항을 설명 합니다. MFC는 OLE를 사용 하는 프로그램을 작성 하는 가장 쉬운 방법은 제공 합니다.  
  
-   활성화를 사용 하도록 OLE 비주얼 편집 (전체).  
  
-   OLE 컨테이너 또는 서버로 작동 합니다.  
  
-   끌어서 놓기 기능을 구현 합니다.  
  
-   날짜 및 시간 데이터를 사용 하 여 작동 합니다.  
  
-   MFC의 상태 데이터를 관리 하려면 모듈을 포함 하 여 내보낸 DLL 함수 시작 지점, OLE/COM 인터페이스 진입점 및 창 프로시저 진입점입니다.  
  
 사용할 수도 있습니다 [Automation](../mfc/automation.md)합니다.  
  
> [!NOTE]
>  OLE 나타내는 기술을 연결 및 포함을 사용 하 여 연결 된 OLE 컨테이너, OLE 서버, OLE 항목, 현재 위치 활성화 (또는 비주얼 편집)를 포함 하 여 추적기를 끌어서 놓기, 용어 및 메뉴 병합 합니다. 활성은 ActiveX 컨트롤 같은 구성 요소 개체 모델 (COM) 및 COM 기반 개체에 적용 됩니다 용어입니다. OLE Automation 자동화를 라고 합니다.  
  
## <a name="in-this-section"></a>섹션 내용  
 [OLE 백그라운드](../mfc/ole-background.md)  
 OLE에 설명 하 고 작동 하는 방법에 대 한 개념 정보를 제공 합니다.  
  
 [활성화](../mfc/activation-cpp.md)  
 OLE 항목을 편집할 경우 활성화의 역할을 설명 합니다.  
  
 [컨테이너](../mfc/containers.md)  
 OLE의 컨테이너를 사용 하 여에 대 한 링크를 제공 합니다.  
  
 [데이터 개체 및 데이터 원본](../mfc/data-objects-and-data-sources-ole.md)  
 사용을 설명 하는 항목에 대 한 링크를 제공 합니다 `COleDataObject` 고 `COleDataSource` 클래스입니다.  
  
 [끌어서 놓기](../mfc/drag-and-drop-ole.md)  
 복사 및 OLE를 사용 하 여 붙여넣기를 사용 하 여 설명 합니다.  
  
 [OLE 메뉴 및 리소스](../mfc/menus-and-resources-ole.md)  
 메뉴 및 MFC OLE 문서 응용 프로그램의 리소스 사용에 설명 합니다.  
  
 [등록](../mfc/registration.md)  
 서버 설치 및 초기화에 설명 합니다.  
  
 [서버](../mfc/servers.md)  
 컨테이너 응용 프로그램에서 사용 하기 위해 OLE 항목 (또는 구성 요소)를 만드는 방법을 설명 합니다.  
  
 [추적기](../mfc/trackers.md)  
 에 대 한 정보를 제공 합니다 `CRectTracker` OLE 클라이언트 항목을 조작할 수 있도록 하기 위한 그래픽 인터페이스를 제공 하는 클래스입니다.  
  
## <a name="related-sections"></a>관련 단원  
 [연결 지점](../mfc/connection-points.md)  
 연결 지점 (이전의 OLE 연결점)를 구현 하는 방법에 설명 MFC 클래스를 사용 하 여 `CCmdTarget` 고 `CConnectionPoint`입니다.  
  
 [컨테이너/서버 COM 구성 요소](../mfc/containers-advanced-features.md)  
 기존 컨테이너 응용 프로그램에 선택적 고급 기능을 통합 하는 데 필요한 단계를 설명 합니다.  
  
 [구성 요소 개체 모델](/windows/desktop/com/the-component-object-model)  
 OLE MFC 없이 사용 하 여 설명 합니다.  
  
## <a name="see-also"></a>참고 항목  
 [개념](../mfc/mfc-concepts.md)

