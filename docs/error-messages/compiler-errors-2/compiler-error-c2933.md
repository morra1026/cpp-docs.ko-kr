---
title: 컴파일러 오류 C2933 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2933
dev_langs:
- C++
helpviewer_keywords:
- C2933
ms.assetid: 394891e3-6b52-4b61-83d2-a1c5125d9bd5
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a251be073402e0eb7ede4a282e18905b23a325bb
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46049893"
---
# <a name="compiler-error-c2933"></a>컴파일러 오류 C2933

'class': type-class-id가 'identifier'의 typedef 멤버로 다시 정의되었습니다.

제네릭 또는 템플릿 클래스를 `typedef` 멤버로 사용할 수 없습니다.

다음 샘플에서는 C2933을 생성합니다.

```
// C2933.cpp
// compile with: /c
template<class T> struct TC { };
struct MyStruct {
   typedef int TC<int>;   // C2933
};

struct TC2 { };
struct MyStruct2 {
   typedef int TC2;
};
```

제네릭을 사용할 때도 C2933이 발생할 수 있습니다.

```
// C2933b.cpp
// compile with: /clr /c
generic<class T> ref struct GC { };
struct MyStruct {
   typedef int GC<int>;   // C2933
};

ref struct GC2 { };
struct MyStruct2 {
   typedef int GC2;
};
```