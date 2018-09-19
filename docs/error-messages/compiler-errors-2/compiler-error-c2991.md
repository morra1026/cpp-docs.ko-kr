---
title: 컴파일러 오류 C2991 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2991
dev_langs:
- C++
helpviewer_keywords:
- C2991
ms.assetid: a87e4404-26e8-4927-b3ee-5d02b3b8bee1
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 09b26d60968b9befc3bc9b027b46f09c269dd9a9
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46091623"
---
# <a name="compiler-error-c2991"></a>컴파일러 오류 C2991

형식 매개 변수 'parameter' 재정의

`parameter`의 두 가지 제네릭 또는 템플릿 정의 간에 형식 충돌이 발생했습니다. 여러 제네릭 또는 템플릿 매개 변수를 정의할 때는 동일한 형식을 사용해야 합니다.

다음 샘플에서는 C2991을 생성합니다.

```
// C2991.cpp
// compile with: /c
template<class T, class T> struct TC {};   // C2991
// try the following line instead
// template<class T, class T2> struct TC {};
```

C2991은 제네릭을 사용하는 경우에도 발생할 수 있습니다.

```
// C2991b.cpp
// compile with: /clr /c
generic<class T,class T> ref struct GC {};   // C2991
// try the following line instead
// generic<class T,class T2> ref struct GC {};
```