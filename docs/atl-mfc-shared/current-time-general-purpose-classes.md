---
title: '현재 시간: 범용 클래스 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- time, setting current
- current time, CTime object
- procedures, getting current time
- initializing objects, with the current time
- time, getting current
ms.assetid: c39e6775-6a92-4b27-95a7-5c86ed371d8a
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 9edf381864121d4e3f6c5a2b6cf7c01198368e1e
ms.sourcegitcommit: 997e6b7d336cddb388bb6e9e56527725fcaa0624
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2018
ms.locfileid: "48860526"
---
# <a name="current-time-general-purpose-classes"></a>현재 시간: 범용 클래스

다음 절차에는 만드는 방법을 보여 줍니다는 `CTime` 개체 및 현재 시간을 사용 하 여 초기화 합니다.

### <a name="to-get-the-current-time"></a>현재 시간을 가져오려면

1. 할당을 `CTime` 개체를 다음과 같이 합니다.

   [!code-cpp[NVC_ATLMFC_Utilities#171](../atl-mfc-shared/codesnippet/cpp/current-time-general-purpose-classes_1.cpp)]

   > [!NOTE]
   > 초기화 되지 않은 `CTime` 개체는 올바른 시간으로 초기화 되지 않았습니다.

1. 호출 된 `CTime::GetCurrentTime` 함수를 운영 체제에서 현재 시간을 가져옵니다. 이 함수는 반환을 `CTime` 의 값을 설정 하는 데 사용할 수 있습니다 `CTime`같이:

   [!code-cpp[NVC_ATLMFC_Utilities#172](../atl-mfc-shared/codesnippet/cpp/current-time-general-purpose-classes_2.cpp)]

   하므로 `GetCurrentTime` 에서 정적 멤버 함수는 `CTime` 클래스 이름 클래스 및 범위 결정 연산자를 사용 하 여 해당 이름을 한 정해야 (`::`), `CTime::GetCurrentTime()`.

물론, 두 단계 이전에 수 결합할 수 단일 프로그램 문이 다음과 같습니다.

[!code-cpp[NVC_ATLMFC_Utilities#173](../atl-mfc-shared/codesnippet/cpp/current-time-general-purpose-classes_3.cpp)]
