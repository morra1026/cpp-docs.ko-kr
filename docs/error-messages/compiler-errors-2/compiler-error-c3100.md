---
title: 컴파일러 오류 C3100
ms.date: 11/04/2016
f1_keywords:
- C3100
helpviewer_keywords:
- C3100
ms.assetid: 7a9c9eaf-08ef-442d-94a0-e457beee8549
ms.openlocfilehash: 07529b576a8ce967c4ff834aab4d6d78d32d52ac
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50521166"
---
# <a name="compiler-error-c3100"></a>컴파일러 오류 C3100

'target': 알 수 없는 특성 한정자

특성 대상은 잘못 지정 되었습니다.

자세한 내용은 [User-Defined Attributes](../../windows/user-defined-attributes-cpp-component-extensions.md)을 참조하세요.

## <a name="example"></a>예제

다음 샘플 C3100를 생성합니다.

```
// C3100.cpp
// compile with: /clr /c
using namespace System;
[AttributeUsage(AttributeTargets::All)]
public ref class Attr : public Attribute {
public:
   Attr(int t) : m_t(t) {}
   int m_t;
};

[invalid_target:Attr(10)];   // C3100
[assembly:Attr(10)];   // OK
```