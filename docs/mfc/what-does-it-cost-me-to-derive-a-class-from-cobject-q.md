---
title: CObject에서 클래스를 파생시키는 비용
ms.date: 11/04/2016
f1_keywords:
- CObject
helpviewer_keywords:
- CObject class [MFC], overhead of derived classes [MFC]
ms.assetid: 9b92c98b-b3dd-48a7-9d24-c3b8554edf90
ms.openlocfilehash: 521b6a32e3e5b34b4da9dab3117d55a728bd8e88
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50500453"
---
# <a name="what-does-it-cost-me-to-derive-a-class-from-cobject"></a>CObject에서 클래스를 파생시키는 비용

클래스에서 파생 하는 오버 헤드 [CObject](../mfc/reference/cobject-class.md) 최소화 됩니다. 파생된 클래스는 4 개의 가상 함수 및 단일 상속 [CRuntimeClass](../mfc/reference/cruntimeclass-structure.md) 개체입니다.

## <a name="see-also"></a>참고 항목

[CObject 클래스: 질문과 대답](../mfc/cobject-class-frequently-asked-questions.md)
