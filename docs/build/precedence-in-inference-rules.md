---
title: 유추 규칙의 우선 순위 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- inference rules in NMAKE
- rules, inference
- precedence, inference rule
ms.assetid: 69e3dc02-0815-4c3a-b02b-1cb85fceaf24
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b4f2e7ff55e935b7e425b552ba85f47f134c6b80
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45725233"
---
# <a name="precedence-in-inference-rules"></a>유추 규칙의 우선 순위

NMAKE 유추 규칙을 여러 번 정의 된 경우 우선 순위가 가장 높은 정의 사용 합니다. 다음은 순위가 가장 높은 우선 순위를 보여 줍니다.

1. 메이크파일의; 정의 유추 규칙 이후 정의 하 고 순위가 키를 누릅니다.

1. Tools.ini;에 정의 된 유추 규칙 이후 정의 하 고 순위가 키를 누릅니다.

1. 미리 정의 된 유추 규칙입니다.

## <a name="see-also"></a>참고 항목

[유추 규칙](../build/inference-rules.md)