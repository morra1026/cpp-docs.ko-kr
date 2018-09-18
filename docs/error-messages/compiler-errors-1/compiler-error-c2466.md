---
title: 컴파일러 오류 C2466 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2466
dev_langs:
- C++
helpviewer_keywords:
- C2466
ms.assetid: 75b251d1-7d0b-4a86-afca-26adedf74486
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 8d43ee9d09fba77db022177a06c6ebe95c65ff79
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46037842"
---
# <a name="compiler-error-c2466"></a>컴파일러 오류 C2466

상수 크기 0의 배열을 할당할 수 없습니다.

배열 할당 되었거나 0 크기를 사용 하 여 선언 됩니다. 배열 크기에 대 한 상수 식에는 0 보다 큰 정수 여야 합니다. 배열 첨자가 0 선언은 Microsoft 확장 이며만 클래스, 구조체 또는 공용 구조체 멤버에 대해서만 유효 ([/Ze](../../build/reference/za-ze-disable-language-extensions.md)).

다음 샘플에서는 C2466 오류가 생성 됩니다.

```
// C2466.cpp
// compile with: /c
int i[0];   // C2466
int j[1];   // OK
char *p;
```