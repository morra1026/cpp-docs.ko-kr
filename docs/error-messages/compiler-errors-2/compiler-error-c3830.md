---
title: 컴파일러 오류 C3830 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3830
dev_langs:
- C++
helpviewer_keywords:
- C3830
ms.assetid: c9798f88-5001-4067-9fb1-09957ddc6fa8
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 20b50d394b0701281cf382c6c0226b0b0b3c8180
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46016847"
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
