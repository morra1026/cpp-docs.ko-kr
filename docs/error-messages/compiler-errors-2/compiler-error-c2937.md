---
title: 컴파일러 오류 C2937 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2937
dev_langs:
- C++
helpviewer_keywords:
- C2937
ms.assetid: 95671ca3-79f7-4b56-a5f2-a92296da1629
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ccb13a7cf95e1f63bd10b3901a3c2157a7fe29bf
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46061807"
---
# <a name="compiler-error-c2937"></a>컴파일러 오류 C2937

'class': type-class-id가 전역 typedef로 재정의되었습니다.

제네릭 또는 템플릿 클래스를 전역 `typedef`로 사용할 수 없습니다.

다음 샘플에서는 C2937을 생성합니다.

```
// C2937.cpp
// compile with: /c
template<class T>
struct TC { };
typedef int TC<int>;   // C2937
typedef TC<int> c;   // OK
```

C2937은 제네릭을 사용하는 경우에도 발생할 수 있습니다.

```
// C2937b.cpp
// compile with: /clr
generic<class T>
ref struct GC { };
typedef int GC<int>;   // C2937
typedef GC<int> xx;   // OK
```