---
title: 컴파일러 오류 C2698 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2698
dev_langs:
- C++
helpviewer_keywords:
- C2698
ms.assetid: 3ebfe395-c20b-4c56-9980-ca9ed8653382
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c7ca3e7568640aabd2b7960d97ea94a11a1d5d59
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46118923"
---
# <a name="compiler-error-c2698"></a>컴파일러 오류 C2698

에 대 한를 사용 하 여 선언을 ' 선언 1'의 기존 using 선언과 공존할 수 없습니다 ' 2' 선언

만든 후는 [선언을 사용 하 여](../../cpp/using-declaration.md) 사용 하 여 모든 데이터 멤버에 대 한 동일한 이름을 사용 하는 동일한 범위에서 선언은 사용할 수 없습니다만 함수를 오버 로드할 수 있습니다.

다음 샘플에서는 C2698를 생성합니다.

```
// C2698.cpp
struct A {
   int x;
};

struct B {
   int x;
};

struct C : A, B {
   using A::x;
   using B::x;   // C2698
}
```