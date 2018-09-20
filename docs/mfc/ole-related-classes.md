---
title: OLE 관련 클래스 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
f1_keywords:
- vc.classes.ole
dev_langs:
- C++
helpviewer_keywords:
- ActiveX classes [MFC]
- OLE classes [MFC]
- OLE [MFC], classes
ms.assetid: 2135cf54-1d9d-4e0e-91b4-943b3440effa
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: f43dadaa4aaefa677106710d1adbcdf0e60be59d
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46411315"
---
# <a name="ole-related-classes"></a>OLE 관련 클래스

이러한 클래스는 다양 한 입력 및 출력 파일에 대 한 예외에 이르는 다양 한 서비스를 제공 합니다.

[COleObjectFactory](../mfc/reference/coleobjectfactory-class.md)<br/>
다른 컨테이너에서 요청 하는 경우 항목을 만드는 데 사용 합니다. 이 클래스의 팩터리를 포함 하 여 보다 구체적인 형식에 대 한 기본 클래스로 사용 됩니다. `COleTemplateServer`합니다.

[COleMessageFilter](../mfc/reference/colemessagefilter-class.md)<br/>
사용 하 여 OLE 경량 원격 프로시저 호출 (LRPC) 동시성을 관리 하는 데 사용 합니다.

[COleStreamFile](../mfc/reference/colestreamfile-class.md)<br/>
COM을 사용 하 여 `IStream` 인터페이스를 `CFile` 복합 파일에 대 한 액세스. 이 클래스 (에서 파생 된 `CFile`) MFC OLE 구조적 저장소를 사용 하는 serialization을 사용 합니다.

[CRectTracker](../mfc/reference/crecttracker-class.md)<br/>
이동, 크기 조정 및 방향 전체 항목을 허용 하는 데 사용 합니다.

## <a name="see-also"></a>참고 항목

[클래스 개요](../mfc/class-library-overview.md)

