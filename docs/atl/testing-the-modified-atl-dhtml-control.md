---
title: 수정 된 ATL DHTML 컨트롤 테스트 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-atl
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- HTML controls, testing
- testing controls
- DHTML controls, testing
ms.assetid: 42316118-9433-410f-9d8a-0efcc1eff824
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 9bd0f1dd58704a49847ebd78de5cee205ad787be
ms.sourcegitcommit: 997e6b7d336cddb388bb6e9e56527725fcaa0624
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2018
ms.locfileid: "48860760"
---
# <a name="testing-the-modified-atl-dhtml-control"></a>수정 된 ATL DHTML 컨트롤 테스트

지금 작동 하는 방법을 확인 하려면 새 컨트롤을 사용해 보세요.

## <a name="to-build-and-test-the-modified-control"></a>빌드 및 수정 된 컨트롤을 테스트 하려면

1. 프로젝트를 다시 빌드하고에서 엽니다 **테스트 컨테이너**합니다. 참조 [속성 및 이벤트 테스트 컨테이너를 사용 하 여 테스트](../mfc/testing-properties-and-events-with-test-container.md) 액세스 하는 방법에 대 한 내용은 **테스트 컨테이너**합니다.

   모든 추가한 단추를 표시 하도록 컨트롤의 크기를 조정 합니다.

1. HTML을 변경 하 여 삽입 하는 두 개의 단추를 검사 합니다. 각 단추에서 식별 된 레이블 갖습니다 [ATL DHTML 컨트롤 수정](../atl/modifying-the-atl-dhtml-control.md): **새로 고침** 하 고 **HelloHTML**합니다.

1. 작동 방식을 확인 하려면 두 개의 새 단추를 테스트 합니다.

이제 UI의 일부분이 아닌 메서드를 테스트 합니다.

1. 테두리를 활성화 하도록 컨트롤을 강조 표시 합니다.

1. 에 **제어** 메뉴에서 클릭 **메서드 호출**합니다.

레이블이 지정 된 목록에서 메서드 **메서드 이름** 컨테이너를 호출할 수 있는 메서드는: `MethodInvoked` 고 `GoToURL`입니다. 다른 모든 메서드는 UI에 의해 제어 됩니다.

1. 선택 메서드를 호출 하 고 클릭 `Invoke` 메서드의 메시지 상자를 표시 하거나 www.microsoft.com로 이동 합니다.

1. 에 **메서드 호출** 대화 상자, 클릭 **닫기**합니다.

다양 한 요소 및 ATL DHTML 컨트롤을 구성 하는 파일에 대 한 자세한 내용은 참조 하세요 [DHTML 컨트롤 프로젝트의 요소 식별](../atl/identifying-the-elements-of-the-dhtml-control-project.md)합니다.

## <a name="see-also"></a>참고 항목

[DHTML 컨트롤에 대 한 지원](../atl/atl-support-for-dhtml-controls.md)
