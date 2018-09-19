---
title: 컴파일러 오류 C2765 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2765
dev_langs:
- C++
helpviewer_keywords:
- C2765
ms.assetid: 47ad86f3-a7e0-47ad-85ff-0f5534458cb9
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 708a4c326e87cf580208e26ef5ffe540afd52f95
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46085136"
---
# <a name="compiler-error-c2765"></a>컴파일러 오류 C2765

'function': 함수 템플릿의 명시적 특수화는 기본 인수를 가질 수 없습니다.

기본 인수는 함수 템플릿의 명시적 특수화에는 허용 되지 않습니다. 자세한 내용은 [명시적 함수 템플릿의 특수화](../../cpp/explicit-specialization-of-function-templates.md)합니다.

다음 샘플에서는 C2765를 생성합니다.

```
// C2765.cpp
template<class T> void f(T t) {};

template<> void f<char>(char c = 'a') {}   // C2765
// try the following line instead
// template<> void f<char>(char c) {}
```