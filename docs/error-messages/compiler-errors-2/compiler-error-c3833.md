---
title: 컴파일러 오류 C3833
ms.date: 11/04/2016
f1_keywords:
- C3833
helpviewer_keywords:
- C3833
ms.assetid: 8152be53-e01e-48cd-9eef-9de38723664c
ms.openlocfilehash: eb320dda9a69937e49f669153bb77e484c5a15fc
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50549593"
---
# <a name="compiler-error-c3833"></a>컴파일러 오류 C3833

'type': pointer_type에 대 한 잘못 된 대상 형식

[interior_ptr](../../windows/interior-ptr-cpp-cli.md) 하거나 [pin_ptr](../../windows/pin-ptr-cpp-cli.md) 잘못 선언 되었습니다.

다음 샘플에서는 C3833 오류가 생성 됩니다.

```
// C3833.cpp
// compile with: /clr

ref class MyClass {
public:
   int data;
   MyClass() : data(35) {}
};

int main() {
   interior_ptr<MyClass> p;   // C3833

   // OK
   MyClass ^ h_MyClass = gcnew MyClass;
   interior_ptr<int> i = &(h_MyClass->data);
   System::Console::WriteLine(*i);
}
```

다음 샘플에서는 C3833 오류가 생성 됩니다.

```
// C3833b.cpp
// compile with: /clr /c
ref class G {
public:
   int i;
};

int main() {
   G ^ pG = gcnew G;
   pin_ptr<G> ppG = &pG;   // C3833 can't pin a whole object

   // OK
   pin_ptr<int> ppG2 = &pG->i;
   *ppG2 = 54;
   int * pi = ppG2;
   System::Console::WriteLine(*pi);
   System::Console::WriteLine(*ppG2);

   *pi = 55;
   System::Console::WriteLine(*pi);
   System::Console::WriteLine(*ppG2);

   *ppG2 = 56;
   System::Console::WriteLine(*pi);
   System::Console::WriteLine(*ppG2);
}
```