---
title: 컴파일러 오류 C3830
ms.date: 11/04/2016
f1_keywords:
- C3830
helpviewer_keywords:
- C3830
ms.assetid: c9798f88-5001-4067-9fb1-09957ddc6fa8
ms.openlocfilehash: 5c484b2b9267bf5f9be3593c20c8b261dafde206
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50631415"
---
# <a name="compiler-error-c3830"></a>컴파일러 오류 C3830

'type1': 값 형식 인터페이스 클래스에서 에서만 상속할 수 'type2'에서 상속할 수 없습니다.

값 형식을 기본 클래스를 상속할 수 없습니다.  자세한 내용은 [클래스 및 구조체](../../windows/classes-and-structs-cpp-component-extensions.md)합니다.

## <a name="example"></a>예제

다음 샘플에서는 C3830 오류가 생성 됩니다.

```
// C3830a.cpp
// compile with: /clr /c
public value struct MyStruct4 {
   int i;
};

public value class MyClass : public MyStruct4 {};   // C3830

// OK
public interface struct MyInterface4 {
   void i();
};

public value class MyClass2 : public MyInterface4 {
public:
   virtual void i(){}
};
```
