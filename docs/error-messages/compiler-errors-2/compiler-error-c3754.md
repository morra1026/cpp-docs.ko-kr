---
title: 컴파일러 오류 C3754
ms.date: 11/04/2016
f1_keywords:
- C3754
helpviewer_keywords:
- C3754
ms.assetid: 14b877bc-9277-40ec-af1c-196a58b45f10
ms.openlocfilehash: e03ac39213429fbbb9f289be3514718985c04b4b
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50582119"
---
# <a name="compiler-error-c3754"></a>컴파일러 오류 C3754

대리 생성자: 멤버 함수 'f'는 'type' 형식의 인스턴스에서 호출할 수 없습니다

함수를 포함 하지 않는 형식에 대 한 포인터를 통해 함수를 호출 했습니다.

## <a name="example"></a>예제

다음 샘플에서는 C3754 오류가 생성 됩니다.

```
// C3754a.cpp
// compile with: /clr
using namespace System;

delegate void MyDel();

interface class MyInterface {};

ref struct MyClass : MyInterface {
   void f() {}
};

int main() {
   MyInterface^ p = gcnew MyClass;
   MyDel^ q = gcnew MyDel(p, &MyClass::f);   // C3754
   // try the following line instead
//   MyDel^ q = gcnew MyDel(safe_cast<MyClass^>(p), &MyClass::f);
}
```
