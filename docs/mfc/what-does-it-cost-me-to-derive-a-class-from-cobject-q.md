---
title: CObject에서 클래스를 파생시키는 비용 | Microsoft 문서
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
f1_keywords:
- CObject
dev_langs:
- C++
helpviewer_keywords:
- CObject class [MFC], overhead of derived classes [MFC]
ms.assetid: 9b92c98b-b3dd-48a7-9d24-c3b8554edf90
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: e41f9060ce24b89a0a7faae54ca6207c740475f3
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46443243"
---
# <a name="what-does-it-cost-me-to-derive-a-class-from-cobject"></a>CObject에서 클래스를 파생시키는 비용

클래스에서 파생 하는 오버 헤드 [CObject](../mfc/reference/cobject-class.md) 최소화 됩니다. 파생된 클래스는 4 개의 가상 함수 및 단일 상속 [CRuntimeClass](../mfc/reference/cruntimeclass-structure.md) 개체입니다.

## <a name="see-also"></a>참고 항목

[CObject 클래스: 질문과 대답](../mfc/cobject-class-frequently-asked-questions.md)
