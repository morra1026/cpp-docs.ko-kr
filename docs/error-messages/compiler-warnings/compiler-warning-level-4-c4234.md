---
title: 컴파일러 경고 (수준 4) C4234 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4234
dev_langs:
- C++
helpviewer_keywords:
- C4234
ms.assetid: f7fecd5c-8248-4fde-8446-502aedc357ca
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a6ce6ba622cb480096144706589a01dee7326f38
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46118234"
---
# <a name="compiler-warning-level-4-c4234"></a>컴파일러 경고(수준 4) C4234

비표준 확장이 사용 됨: 'keyword' 키워드를 사용 하도록 예약

컴파일러는 사용 하는 키워드를 아직 구현 하지 않습니다.

이 경고는 오류를 자동으로 승격 됩니다. 사용 하 여이 동작을 수정 하려는 경우 [#pragma 경고](../../preprocessor/warning.md)합니다. 예를 들어 수준 4 경고 문제가 c4234

```
#pragma warning(2:4234)
```

소스 코드 파일.