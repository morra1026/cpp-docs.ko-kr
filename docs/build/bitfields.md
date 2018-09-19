---
title: 비트 필드 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- bitfields
ms.assetid: e9a1010d-1e1b-487f-9943-3c574e08f544
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a7451ea6afee81cc296fb091705bde48041ef5d1
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45722490"
---
# <a name="bitfields"></a>비트 필드

구조 비트 필드는 64 비트 제한 되 고 형식이 될 수 있습니다, 부호 없는 int, int64, 정수나 부호 없는 int64를 서명 합니다. 형식 경계를 교차 하는 비트 필드는 다음 형식 맞춤을 비트 필드에 맞게 비트를 건너뜁니다. 예를 들어 정수 넘어설 수 없습니다는 32 비트 경계입니다.

## <a name="see-also"></a>참고 항목

[형식 및 저장소](../build/types-and-storage.md)