---
title: 컴파일러 오류 C3210 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3210
dev_langs:
- C++
helpviewer_keywords:
- C3210
ms.assetid: c6e9d309-fabc-4e7d-b526-be20d9fe3f6a
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 804586a866f6a4d2c3cf206af14e0e2f907ed1b6
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46037114"
---
# <a name="compiler-error-c3210"></a>컴파일러 오류 C3210

'type': 액세스 선언은 기본 클래스 멤버에만 적용할 수 있습니다

A [선언을 사용 하 여](../../cpp/using-declaration.md) 잘못 지정 되었습니다.

## <a name="example"></a>예제

다음 샘플 C3210를 생성합니다.

```
// C3210.cpp
// compile with: /c
struct A {
protected:
   int i;
};

struct B {
   using A::i;   // C3210
};

struct C : public A {
   using A::i;   // OK
};
```