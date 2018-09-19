---
title: 컴파일러 오류 C2157 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2157
dev_langs:
- C++
helpviewer_keywords:
- C2157
ms.assetid: babbca24-16dc-4b69-be14-a675029249c1
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: bd17b03cc48555800e3c36cc3f5512506f011372
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46072077"
---
# <a name="compiler-error-c2157"></a>컴파일러 오류 C2157

'function': pragma 목록에서 사용하려면 먼저 선언해야 합니다.

함수 이름이 선언되지 않은 상태에서 [alloc_text](../../preprocessor/alloc-text.md) pragma에 대한 함수 목록에서 참조되었습니다.

다음 샘플에서는 C2157을 생성합니다.

```
// C2157.cpp
// compile with: /c
#pragma alloc_text( "func", func)   // C2157

// OK
extern "C" void func();
#pragma alloc_text( "func", func)
```