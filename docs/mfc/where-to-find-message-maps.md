---
title: 메시지 맵의 찾을 장소 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- macros, message map
- locating message maps
- message classes [MFC], finding
- message-map macros
ms.assetid: bf59fbc8-b222-42d3-b5d3-0a79aa3cb923
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 81958eda508a3e0b4b93ac0d169f3aa3bfece2a2
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46434273"
---
# <a name="where-to-find-message-maps"></a>메시지 맵을 찾을 장소

응용 프로그램 마법사를 사용 하 여 새 기본 응용 프로그램을 만들 때 응용 프로그램 마법사를 만들면 각 명령 대상 클래스에 대 한 메시지 맵을 작성 합니다. 이 파생된 응용 프로그램, 문서, 뷰 및 프레임 창 클래스를 포함합니다. 특정 메시지와 미리 정의 된 명령에 대 한 응용 프로그램 마법사에 의해 제공 항목이 이미 이러한 메시지 맵의 일부 및 일부는 추가할 처리기에 대 한 자리 표시자 일 뿐입니다.

클래스의 메시지 맵을 합니다. 클래스에 대 한 CPP 파일입니다. 응용 프로그램 마법사에서 만들어지는 기본 메시지 맵을 사용 하 여 작업을 사용 하 여 속성 창 메시지 및 명령을 처리 하는 각 클래스에 대 한 항목을 추가. 일반적인 메시지 맵 일부 항목을 추가 하면 다음과 같습니다.

[!code-cpp[NVC_MFCMessageHandling#1](../mfc/codesnippet/cpp/where-to-find-message-maps_1.cpp)]

메시지 맵 매크로의 컬렉션으로 구성 됩니다. 두 매크로 [BEGIN_MESSAGE_MAP](reference/message-map-macros-mfc.md#begin_message_map) 하 고 [END_MESSAGE_MAP](reference/message-map-macros-mfc.md#end_message_map), 메시지 맵에서 대괄호입니다. 다른 매크로 같은 `ON_COMMAND`, 메시지 지도의 내용을 입력 합니다.

> [!NOTE]
>  메시지 맵 매크로 세미콜론 뒤 없습니다.

클래스 추가 마법사를 사용 하 여 새 클래스를 만들 때 클래스에 대 한 메시지 맵을 제공 합니다. 또는 소스 코드 편집기를 사용 하 여 수동으로 메시지 맵을 만들 수 있습니다.

## <a name="see-also"></a>참고 항목

[프레임워크가 메시지 맵을 검색하는 방법](../mfc/how-the-framework-searches-message-maps.md)

