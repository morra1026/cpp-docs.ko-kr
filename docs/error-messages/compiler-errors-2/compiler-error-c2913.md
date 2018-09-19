---
title: 컴파일러 오류 C2913 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2913
dev_langs:
- C++
helpviewer_keywords:
- C2913
ms.assetid: c6cf6090-02e8-49a5-913f-5bc6f864b769
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 6da5d739c4dd9ccec71c26a3fc9101cde1535ce3
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46103128"
---
# <a name="compiler-error-c2913"></a>컴파일러 오류 C2913

명시적 특수화 'declaration' 클래스 템플릿의 특수화 아닙니다.

템플릿이 아닌 클래스를 특수화할 수 없습니다.

다음 샘플에서는 C2913 오류가 생성 됩니다.

```
// C2913.cpp
// compile with: /c
class X{};
template <class T> class Y{};

template<> class X<int> {};   // C2913
template<> class Y<int> {};
```