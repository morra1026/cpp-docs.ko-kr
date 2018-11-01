---
title: 집계
ms.date: 11/04/2016
helpviewer_keywords:
- aggregation [C++]
- aggregate objects [C++]
ms.assetid: 7125bb8e-b269-4b50-9bba-295b467a54cc
ms.openlocfilehash: d5a09dcd8c289447491ebc7111a77549166a7d00
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50633415"
---
# <a name="aggregation"></a>집계

경우는 개체의 구현 자가 하려는 다른, 미리 작성 된 개체에서 제공 하는 서비스를 활용 하는 경우가 있습니다. 또한이 두 번째 개체를 첫 번째의 일부로 표시 되도록 하려고 합니다. COM 달성 둘 다 포함 하 고 집계를 통해 이러한 목표입니다.

집계 (외부) 포함 하는 개체 생성 과정의 일부로 포함 된 (내부) 개체를 만들고 내부 개체의 인터페이스는 외부에 의해 노출 되 있음을 의미 합니다. 개체 자체를 여부 집계할 수 있습니다. 이 경우 제대로 작동 하려면 집계에 대 한 특정 규칙을 수행 해야 합니다.

기본적으로, 모든 `IUnknown` 포함 된 개체에 대 한 메서드 호출을 포함 하는 개체를 위임 해야 합니다.

## <a name="see-also"></a>참고 항목

[COM 소개](../atl/introduction-to-com.md)<br/>
[개체 다시 사용](/windows/desktop/com/reusing-objects)

