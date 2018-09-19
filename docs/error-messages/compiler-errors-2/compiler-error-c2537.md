---
title: 컴파일러 오류 C2537 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2537
dev_langs:
- C++
helpviewer_keywords:
- C2537
ms.assetid: aee81d8e-300e-4a8b-b6c4-b3828398b34e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 65db4fa66d147cc46c1a6013d07048892dfa0800
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46136025"
---
# <a name="compiler-error-c2537"></a>컴파일러 오류 C2537

'specifier': 링크 사양이 올바르지 않습니다

가능한 원인:

1. 링크 지정 자가 지원 되지 않습니다. "C" 링크 지정자만 지원 됩니다.

1. "C" 링크가 둘 이상의 함수 오버 로드 된 함수 집합에 대해 지정 됩니다. 이것은 허용되지 않습니다.

다음 샘플에서는 C2537를 생성합니다.

```
// C2537.cpp
// compile with: /c
extern "c" void func();   // C2537
extern "C" void func2();   // OK
```