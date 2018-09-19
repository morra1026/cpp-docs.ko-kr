---
title: 컴파일러 오류 C2584 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2584
dev_langs:
- C++
helpviewer_keywords:
- C2584
ms.assetid: 836e2c0a-86c0-4742-b432-beb0191ad20e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f0f8c523936473673f3af09400922e2594ed1891
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46029431"
---
# <a name="compiler-error-c2584"></a>컴파일러 오류 C2584

'Class': 직접 기본 'Base2' 액세스할 수 있음 이미 'Base1'의 기본

`Class` 직접 파생 이미 `Base1`합니다. `Base2` 파생 되기도 `Base1`합니다. `Class` 파생 될 수 없습니다 `Base2` 에서 간접적으로 상속 의미 하므로 `Base1` 다시는 유효 하지 않은 때문에 `Base1` 이미 직접 기본 클래스입니다.

## <a name="example"></a>예제

다음 샘플 C2584를 생성합니다.

```
// C2584.cpp
// compile with: /c
struct A1 {
   virtual int MyFunction();
};

struct A2 {
    virtual int MyFunction();
};

struct B1: public virtual A1, virtual A2 {
    virtual int MyFunction();
};

struct B2: public virtual A2, virtual A1 {
    virtual int MyFunction();
};

struct C: virtual B1, B2 {
    virtual int MyFunction();
};

struct Z : virtual B2, virtual C {   // C2584
// try the following line insted
// struct Z : virtual C {
    virtual int MyFunction();
};
```