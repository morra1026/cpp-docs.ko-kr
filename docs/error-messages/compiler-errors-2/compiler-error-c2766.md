---
title: 컴파일러 오류 C2766 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2766
dev_langs:
- C++
helpviewer_keywords:
- C2766
ms.assetid: 8032f4ca-6827-4f04-9c61-c44643c85cc4
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ee59a8ebc0de3c539d1c9b775dcf06525b1a77fa
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46051531"
---
# <a name="compiler-error-c2766"></a>컴파일러 오류 C2766

명시적 특수화 'specialization'가 이미 정의 되어

중복 된 명시적 특수화는 허용 되지 않습니다. 자세한 내용은 [명시적 함수 템플릿의 특수화](../../cpp/explicit-specialization-of-function-templates.md)합니다.

다음 샘플에서는 C2766 오류가 생성 됩니다.

```
// C2766.cpp
// compile with: /c
template<class T>
struct A {};

template<>
struct A<int> {};

template<>
struct A<int> {};   // C2766
// try the following line instead
// struct A<char> {};
```