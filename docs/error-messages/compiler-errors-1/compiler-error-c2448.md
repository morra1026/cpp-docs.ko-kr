---
title: 컴파일러 오류 C2448 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2448
dev_langs:
- C++
helpviewer_keywords:
- C2448
ms.assetid: e255df3c-f861-4b4d-a193-8768cef061a5
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b5d3de3b8d4d5d184bb33214679842c557aadf7d
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46135998"
---
# <a name="compiler-error-c2448"></a>컴파일러 오류 C2448

'identifier': 함수 스타일 이니셜라이저가 함수 정의에 표시 됩니다.

함수 정의 올바르지 않습니다.

이 오류는 이전 스타일 C 언어 형식 목록에서 발생할 수 있습니다.

다음 샘플에서는 C2448 오류가 생성 됩니다.

```
// C2448.cpp
void func(c)
   int c;
{}   // C2448
```