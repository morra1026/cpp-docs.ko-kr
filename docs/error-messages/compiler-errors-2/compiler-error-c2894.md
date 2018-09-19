---
title: 컴파일러 오류 C2894 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2894
dev_langs:
- C++
helpviewer_keywords:
- C2894
ms.assetid: 4e250579-2b59-4993-a6f4-49273e7ecf06
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 14305b88042421817133a3def8fd73db57055026
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46095731"
---
# <a name="compiler-error-c2894"></a>컴파일러 오류 C2894

'C' 링크가에 템플릿은 선언할 수 없습니다.

이 오류 때문일 수 있습니다 내에 정의 된 템플릿으로 `extern` "C" 블록입니다.

다음 샘플에서는 C2894를 생성합니다.

```
// C2894.cpp
extern "C" {
   template<class T> class stack {};   // C2894 fail

   template<class T> void f(const T &aT) {}   // C2894
}
```

다음 샘플에서는 C2894를 생성합니다.

```
// C2894b.cpp
// compile with: /c
extern "C" template<class T> void f(const T &aT) {}   // C2894

template<class T> void f2(const T &aT) {}   // OK
```