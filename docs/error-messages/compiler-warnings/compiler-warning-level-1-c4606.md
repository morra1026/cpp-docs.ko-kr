---
title: 컴파일러 경고 (수준 1) C4606 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4606
dev_langs:
- C++
helpviewer_keywords:
- C4606
ms.assetid: c1b45fb6-672b-42eb-9e1c-c67b3e4150d3
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: bcdaba046f495dc3a29a7c9228edc561674f568f
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46035996"
---
# <a name="compiler-warning-level-1-c4606"></a>컴파일러 경고(수준 1) C4606

\#pragma 경고: 'warning_number'가 무시 됩니다. 코드 분석 경고가 경고 수준과 연결 되어 있지 않습니다.

코드 분석 경고에 `error`, `once`, 및 `default` 지원 되는 [경고](../../preprocessor/warning.md) pragma입니다.

## <a name="example"></a>예제

다음 샘플 C4606을 생성합니다.

```
// C4606.cpp
// compile with: /c /W1
#pragma warning(1: 6001)   // C4606
#pragma warning(once: 6001)   // OK
```