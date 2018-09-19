---
title: 컴파일러 오류 C2754 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2754
dev_langs:
- C++
helpviewer_keywords:
- C2754
ms.assetid: 1cab66c5-da9d-4b81-b7fb-9cdc48ff1ccc
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 67338d647ce1774699973b8f498da9a8887eff11
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46095666"
---
# <a name="compiler-error-c2754"></a>컴파일러 오류 C2754

'specialization': 부분 특수화는 종속적 비형식 템플릿 매개 변수를 사용할 수 없습니다

부분적으로 종속적 비형식 템플릿 매개 변수가 있는 템플릿 클래스 특수화 하려고 했습니다. 이것은 허용되지 않습니다.

다음 샘플에서는 C2754를 생성합니다.

```
// C2754.cpp
// compile with: /c

template<class T, T t>
struct A {};

template<class T, int N>
struct B {};

template<class T> struct A<T,5> {};   // C2754
template<> struct A<int,5> {};   // OK
template<class T> struct B<T,5> {};   // OK
```